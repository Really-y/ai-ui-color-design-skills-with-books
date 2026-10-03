# Principles and concepts — Brad Frost, *Atomic Design* (2016)

Each entry: name, Frost's definition, why it matters, how to apply it, pitfalls. Chapter references in
parentheses so claims can be checked against the book.

## Contents

1. Why pages fail: scope components, not pages (ch. 1)
2. Modularity across strategy, process, content, code, visual design (ch. 1)
3. Design atmosphere, style tiles, element collages (ch. 1, ch. 4)
4. UI frameworks: pros, cons, "tiny Bootstraps for every client" (ch. 1)
5. Style guide types (ch. 1)
6. Style guide benefits (ch. 1, ch. 3)
7. Style guide challenges (ch. 1)
8. The five stages of atomic design (ch. 2)
9. "A mental model, not a linear process" (ch. 2)
10. The part and the whole; structure vs content (ch. 2)
11. Naming the stages; atomic design is for all UIs (ch. 2)
12. Pattern library mechanics: nesting dolls, includes, data, pseudo-patterns (ch. 3)
13. Qualities of an effective pattern library (ch. 3)
14. People first; when to start; pitching (ch. 4)
15. Interface inventory (ch. 4) — see interface-inventory.md
16. Ask forgiveness, not permission; the Lego pile (ch. 4)
17. Redefining design beyond aesthetics; death to the waterfall (ch. 4)
18. Development is design; the front-end prep chef (ch. 4)
19. Iteration as subtractive sculpture; establishing direction (ch. 4)
20. Comps as hypotheses; deciding in the browser (ch. 4)
21. Artifact vs product; design-system-first; friendly friction (ch. 5)
22. Makers and users; team makeup (ch. 5)
23. Governance and the three types of pattern change (ch. 5)
24. The holy grail and its technical bridges (ch. 5)
25. The ten "make it ..." maintenance principles (ch. 5)

---

## 1. Why pages fail: scope components, not pages (ch. 1)

**Definition.** The page metaphor comes from the document-sharing origins of the web (Berners-Lee at
CERN). It still helps users (bookmarks, pagination), but it is a bad unit for *scoping and building*
work, because it assumes "a page is a uniform, isolated, quantifiable thing" when the web is "a fluid,
interactive, interdependent medium".

**Why.** "How long will the homepage take?" depends entirely on what is on it: a tagline and a
background image could be done by lunch; carousels, dynamic forms and third-party integrations could
take months. A "30,000-page university website" may really be three content types and two layouts.

**Apply.** Estimate and plan by the functionality and components contained in pages, never by page
count. When someone says "five-page website" or "redesign 30,000 pages", translate to a list of
content types, layouts and components before answering.

**Pitfall.** Treating the homepage or the page count as the unit of effort; forgetting that the same
component appears across many pages.

## 2. Modularity across strategy, process, content, code, visual design (ch. 1)

**Definition.** Modularity (Ford's interchangeable parts; OOP's separation of concerns and single
responsibility principle) applied to every aspect of web creation. It "matters more than ever"
because of the explosion of devices, viewports and environments (Future-Friendly manifesto:
"Disruption will only accelerate").

**How it shows up (ch. 1):**
- *Strategy:* stop the bulldoze-and-replace redesign every three to eight years. Big redesigns knock
  users off Jared Spool's "Magic Escalator of Acquired Knowledge" and, without a process change,
  "New-And-Shiny today becomes Old-And-Crusty tomorrow". Ship minimum viable products, iterate.
- *Process:* capital-A Agile (Scrum, Lean, the manifesto) vs lowercase-a agile (an informal desire for
  an efficient process). Brett Harned: "we won't ever truly be Agile ... That's okay, as long as we say
  what we will be." Keep what matters: cross-disciplinary teams, get into the final environment faster,
  ship early and often, break big tasks into smaller components.
- *Content:* "Team Chunk" — structured, modular content that can go anywhere (NPR's COPE: Create Once,
  Publish Everywhere; Karen McGrane's well-structured chunks).
- *Code:* JavaScript patterns and architectures; OOCSS, SMACSS, BEM for modular CSS.
- *Visual design:* see principle 3.

**Pitfall.** "We're trying to be more agile" as a slogan without saying concretely what you will be.

## 3. Design atmosphere, style tiles, element collages (ch. 1, expanded ch. 4)

**Definition.** Static mockups of every page are untenable; Stephen Hay: fully baked Photoshop comps
are "the most effective way to show your clients what their website will never look like." Static
tools remain valuable for establishing **design atmosphere** (Andy Clarke): "the feelings we get that
are evoked by colour, texture and typography ... independent of arrangement and visual placement. It
will be seen, or felt, at every screen size and on every device."

- **Style tiles** (Samantha Warren): one-pager of colour, type and texture explorations; more tangible
  than a mood board, less than a comp. In-browser counterpart: style prototypes.
- **Element collages** (Dan Mall): an "exploded collage of interface elements" that applies the
  atmosphere to actual UI elements, free of layout and polish.

**Why.** Breaking visual exploration into chunks saves time, avoids presenting "unrealistic,
premature layouts", and "shifts stakeholders away from simply reacting to a pretty picture" toward
conversations about direction and project goals. They also educate stakeholders in pattern thinking
(ingredients, not pages).

**Apply.** Order: 20-second gut test -> style tiles -> element collages -> (only then) full comps for
context. See playbook.md "Establishing visual direction".

## 4. UI frameworks: pros, cons, "tiny Bootstraps for every client" (ch. 1)

**Pros** of Bootstrap/Foundation: speed, rapid prototypes, cross-browser-tested patterns, community
support; MVPs launch sooner.

**Cons** (Frost's list):
1. *Look-alike* — "sci-fi jumpsuits": Nike, Adidas, Puma and Reebok on Bootstrap would look
   substantially similar; customising eventually means fighting the framework's structure, style and
   functionality.
2. *Bloat* — users download the framework's unused CSS and JS.
3. *Not far enough* — a threshold is crossed where time modifying, extending and fixing outweighs the
   initial speed benefit.
4. *Naming* — you subscribe to someone else's structure and naming ("jumbotron"); discuss how the
   framework's naming fits your codebase and workflow *before* adopting.

**Resolution.** Conceptually frameworks are right; Dave Rupert: make "tiny Bootstraps for every
client" — responsive deliverables as "fully-functioning Twitter Bootstrap-style systems custom tailored
for your clients' needs ... living code samples [that] are self-documenting style guides". "It's not
just about using a design system, it's about creating your system."

## 5. Style guide types (ch. 1)

Style guides are "the cornerstones of good design systems": they "document and organize design
materials while providing guidelines, usage, and guardrails."

| Type | Contents | Notes |
|---|---|---|
| Brand identity | logos, typography, colour palettes, messaging (mission, taglines), collateral (business cards, PowerPoint templates), Pantone values | one centralized hub; fairly tactile, relatively fixed (WVU) |
| Design language | overarching design direction, philosophy, principles plus specific applications | Google material design; incorporates other types; *not* set in stone (material will one day be replaced; the brand stays) |
| Voice and tone | how voice/tone shift per scenario | Kate Kiefer Lee: "voice stays the same from day to day, but its tone has to change all the time"; MailChimp: credit card declined -> drop the cheeky tone |
| Writing | guidelines/guardrails for many contributing authors | can be granular (punctuation, grammar) or a concise list of principles (Dalhousie; The Economist) |
| Code | conventions, patterns, examples for how teams write code | GitHub's guide (HTML, CSS, JS, Ruby) |
| Pattern library | a.k.a. front-end style guide, UI library, component library — the UI patterns themselves | "the main event"; the rest of the book (Code for America) |

Later (ch. 5, "make it bigger"): house all of these in one hub (Intuit Harmony).

## 6. Style guide benefits (ch. 1; restated as a list in ch. 3)

1. **Consistency and cohesion.** Health-insurer anecdote: five clicks, four distinct interface designs
   -> user burden and distrust at the payment form. Reuse of patterns; third parties (payment portals,
   localized sites) can match the primary experience. Result: UIs feel "united and trustworthy", users
   master them faster.
2. **Shared vocabulary.** "What does 'utility toolbar' mean?" Disciplines name the same module
   differently; individuals "go rogue". Naming patterns ("Blocks Three-Up" at Starbucks) lets everyone
   speak the same language.
3. **Education.** Anna Debenham: "Education is as important as documentation. A style guide can show
   clients that websites are systems rather than collections of pages." Relieves **special snowflake
   syndrome** (departments believing they have unique problems and demanding unique solutions).
4. **Empathetic workflow.** Designers and developers are "forced to think about how their decisions
   affect the broader design system"; harder to go rogue. The guide becomes a hub for each discipline's
   considerations.
5. **Testing.** "The homepage is broken? Well, what exactly is breaking it?" Isolated patterns let
   developers zero in on errors, browser inconsistencies, performance issues.
6. **Speed.** Big up-front cost, then much faster. MailChimp built patterns from the four primary
   screens of the app and found they worked everywhere else (Federico Holgado).
7. **Long haul.** Value increases over time "like a fine wine"; fold in lessons from analytics, user
   testing and A/B testing; even a major redesign keeps forms, buttons, headings.

Ch. 3 list adds: easier cross-browser/device, performance and accessibility testing; a
future-friendly foundation; vocabulary that includes outside vendors.

## 7. Style guide challenges (ch. 1)

| Challenge | What Frost says | Counter (where in book) |
|---|---|---|
| The hard sell | short-term, quarter-by-quarter mindset vs a long-term investment | pitch in time and money (ch. 4) |
| Time | Dennis Crowley: "The hard part is building the machine that builds the product." Aggressive timelines and finite budgets detract | prep-chef, piggyback on a project (ch. 4) |
| Auxiliary project | treated as separate from the core product -> "nice to have" -> first on the chopping block. Same fallacy as "we wish we had budget for accessibility" | bake it into the workflow whether or not the plan calls for it (ch. 4) |
| Maintenance and governance | guides "die on the vine"; thrown out beside PSDs and wireframes without a strategy for who manages, maintains, enforces | ch. 5 |
| Audience confusion | seen as only for designers/developers -> "a best-kept secret guarded by one discipline"; too vague or too technical | cross-disciplinary, approachable (ch. 5) |
| Structure | must convey what it is and why it matters; attractive, inviting, visible, clear, easy to use (Yelp's intro text names purpose and audience) | approachable (ch. 5) |
| Lack of context | most libraries don't say when/how/where components are used, so nobody knows how global a pattern is or which pages to QA after a change ("Highlight Block") | lineage (ch. 3), contextual (ch. 5) |
| Lacking a methodology | many libraries are "loosely arranged sprays of modules" | atomic design (ch. 2) |

## 8. The five stages of atomic design (ch. 2)

Borrowed from chemistry: atoms (smallest functional unit, distinct properties) combine into
molecules (groups of two or more atoms with their own new properties) which combine into organisms
(assemblies of molecules functioning as a unit). Josh Duck's Periodic Table of HTML Elements shows all
interfaces are made of the same finite set of elements.

| Stage | Frost's definition | Examples | Role in the library |
|---|---|---|---|
| **Atoms** | "foundational building blocks ... basic HTML elements like form labels, inputs, buttons, and others that can't be broken down any further without ceasing to be functional." Each has intrinsic properties (dimensions of a hero image, font size of a primary heading) | label, input, button, logo image, icon, heading, thumbnail | "demonstrate all your base styles at a glance"; "don't exist in a vacuum and only really come to life with application" |
| **Molecules** | "relatively simple groups of UI elements functioning together as a unit" | label + search input + button = search form; thumbnail + headline + excerpt = block-post | combined atoms "suddenly have purpose"; a "simple, portable, reusable component"; enforces the **single responsibility principle** ("do one thing and do it well"); simpler molecules = easier testing, reuse, consistency |
| **Organisms** | "relatively complex UI components composed of groups of molecules and/or atoms and/or other organisms. These organisms form distinct sections of an interface." | header (logo atom + primary nav molecule + search molecule); product grid (one product-item molecule repeated, as on Gap's category page); Instagram photo organism | give context; show simpler parts in action; reusable sections (product grid in category listings, search results, related products) |
| **Templates** | "page-level objects that place components into a layout and articulate the design's underlying content structure." Chemistry analogy ends here deliberately, so stakeholders don't think "you're a bit crazy" | homepage template: header, hero, sections, footer | prove "the parts add up to a well-functioning whole"; show the content *skeleton*: image sizes, character lengths for headings and text passages (Time Inc. template) |
| **Pages** | "specific instances of templates that show what a UI looks like with real representative content in place." The most concrete stage; what users see and stakeholders sign off | homepage with real headline and photo | **test the resilience of the system** ("Does everything look great and function as it should? If the answer is no, then we can loop back and modify our molecules, organisms, and templates"); articulate **variations** |

Frost's one-line summary (ch. 2): atoms = UI elements that can't be broken down further; molecules =
collections of atoms forming relatively simple UI components; organisms = relatively complex components
forming discrete sections of an interface; templates = place components within a layout and demonstrate
the underlying content structure; pages = apply real content to templates and articulate variations to
demonstrate the final UI and test the system's resilience.

**Page-level variations Frost names** (ch. 2): a cart with one item vs ten; a dashboard that normally
shows recent activity but suppresses it for first-time users; a 40-character headline vs a 340-character
one; admin users seeing extra buttons. "The underlying templates are the same, but the user interfaces
change to reflect the dynamic nature of the content."

Mark Boulton (ch. 2): "You can create good experiences without knowing the content. What you can't do
is create good experiences without knowing your content structure. What is your content made from, not
what your content is."

See classify-component.md for the decision guide.

## 9. "A mental model, not a linear process" (ch. 2)

**Definition.** "Atomic design is not a linear process, but rather a mental model to help us think of
our user interfaces as both a cohesive whole and a collection of parts at the same time." The five
stages "concurrently work together".

**Why.** "It would be foolish to design buttons and other elements in isolation, then cross our fingers
and hope everything comes together to form a cohesive whole."

**Apply.** Never run it as "Step 1 atoms, Step 2 molecules ... Step 5 pages". Work on a pattern and its
page context at the same time (ch. 4: the TechCrunch header was built as a pattern *and* included in
every template from day one). Also, atomic design "has nothing to do with web-specific subjects like
CSS or JavaScript architecture" — it is technology-agnostic.

## 10. The part and the whole; structure vs content (ch. 2)

- **Traversal between abstract and concrete.** Frank Chimero's painter steps back from the canvas and
  returns: "a tight feedback loop between mark-making and mark-assessing." Zoom into one component to
  make it "functional, usable, and beautiful", then check it in the context of the final UI. "The parts
  of our designs influence the whole, and the whole influences the parts."
- **Clean separation between structure and content.** Mark Boulton: "It's not 'content then design', or
  'content or design'. It's 'content and design'." Templates hold the content-structure skeleton; pages
  hold the final content; the two influence each other. Example: a list of person-block molecules — if a
  real name "were to wrap onto five lines within the pattern, we would need to address that broken
  behavior at a more atomic level."

## 11. Naming the stages; atomic design is for all UIs (ch. 2)

- Why not "modules/components/elements"? Because "a sense of hierarchy can't be deduced from the names
  alone"; atoms/molecules/organisms imply hierarchy to anyone with basic chemistry.
- But "naming things is hard and imperfect" and "atomic design is not rigid dogma". GE Design (Jeff
  Crossman) met "confused looks" and renamed to Principles, Basics, Components, Templates, Features,
  Applications. "By establishing a taxonomy that made sense for their organization, everyone was able
  to get on board." Choose whatever taxonomy helps your organization communicate.
- Applies to any UI: Word, Keynote, Photoshop, an ATM, native apps. Instagram walk-through: atoms =
  icons, text elements, primary image, avatar; molecules = bottom nav bar, photo-actions bar; organism =
  photo organism (user info, timestamp, photo, actions, like count, caption) stacked endlessly;
  template = layout with the exposed content skeleton (handle, avatar, photo, like count, caption);
  page = real content.

## 12. Pattern library mechanics (ch. 3)

Taught through Pattern Lab (static site generator for atomic design systems; a pattern documentation
and annotation tool; a pattern starter kit — *not* a UI framework, not language/library/style-
dependent, not a CMS). Its deliberately plain look avoids being mistaken for suggested styles.

- **Russian nesting dolls.** Atoms are included inside molecules, molecules inside organisms, organisms
  inside templates. This keeps things **DRY**: change a pattern once and every instance updates — vs
  "sifting through hundreds of Photoshop documents".
- **Includes** (Mustache, logicless templating): `{{> atoms-thumb }}`, `{{> molecules-block-post }}`,
  `{{> organisms-header }}`. Folder/category labels can be renamed; "the most important consideration is
  to establish naming and categorization that is most effective for your team."
- **Named instances.** Wrapping an include in a Mustache section
  (`{{# factoid-advertising }}{{> organisms-factoid }}{{/ factoid-advertising }}`) gives the instance a
  unique name so its content can be swapped. "The final interface is one instantiation of its
  underlying design system."
- **Dynamic data.** Defaults in `/source/data.json` (text, image paths); page-level overrides in a JSON
  file named after the page pattern (`00-homepage.json`): "Lorem Ipsum" + grayscale FPO (for-placement-
  only) image at template level becomes "Moving People" + a real photo at page level. Also YAML,
  Markdown; booleans, arrays/loops.
- **Pseudo-patterns.** `dashboard~admin.json` (tilde) inherits `dashboard.json` and appends/overrides
  (`"isAdmin": true`); the pattern conditionally includes `{{# isAdmin }}{{> molecules-block-actions }}
  {{/ isAdmin }}`. One variable can alter the whole UI (navigation, extra panels, controls).
- **Benefits of designing with data:** clear separation of structure and content (agnostic, flexible
  patterns; DRY); an ad hoc CMS (no WordPress/Drupal just to show variations); a blueprint for back-end
  developers (which bits are static vs dynamic); non-developers (writers, content people, designers)
  can edit content safely, sparing developers "death by a million paper cuts".
- **Viewport tools.** Fluid components are more resilient (a gallery slider full-bleed, in an article,
  in a sidebar — the promise of container queries). Early tools fixated on 320px, 480px, 768px; the
  **ish.** resizer gives randomized small-ish/medium-ish/large-ish viewports so teams consider "the
  entire resolution spectrum". Most useful as a client/colleague education tool.
- **Code view.** Show HTML; optionally CSS/JS (Salesforce Lightning shows HTML + SCSS). Lonely Planet's
  Rizzo shows the *include* code instead because library and production are in sync. Speeds work
  (copy/paste) and lets leads enforce syntax conventions.
- **Living documentation and annotations.** Giant PDF specs get thrown away; documentation "should be
  baked into the living, breathing design system" and hold every discipline's insights (accessibility,
  performance, aesthetics...). Pattern Lab: `pattern-name.md` descriptions; numbered annotations
  clickable in the live UI.
- **Pattern lineage.** "Great, but where is this component actually used?" Lineage shows what a
  component is made of (media-block contains atoms-square and molecules-button-bar) and where it is
  used (media-block-list organism). Use it to know what to retest after a change and to weed out
  redundant/underused patterns before launch.

## 13. Qualities of an effective pattern library (ch. 3)

Whatever tool you choose, look for:
1. pattern descriptions and annotations;
2. the relevant HTML, templating, CSS and/or JavaScript code;
3. viewing patterns across the entire resolution spectrum;
4. showcasing pattern variations (active/disabled tabs);
5. dynamically adding real representative content into pattern structures;
6. contextual information: what makes up a component and where it is used.

"It's not about the tools we use to create pattern libraries, but rather how we use them." Choose a
tool that fits your infrastructure and how the team works.

## 14. People first; when to start; pitching (ch. 4)

- "It all comes down to people truly collaborating and communicating." Mark Boulton: "The design
  process is weird and complicated, because people are weird and complicated." Tools and talent without
  cooperation yield "disappointing shades of bad work".
- **When:** "now". Piggyback on a redesign, replatform or other initiative, or win a dedicated project.
- **Pitching:** education plus marketing savvy. Reframe: "Do you like saving time and money? Yes or
  no?" then pitch every benefit through time and money (cohesion -> users master the UI -> conversions;
  reuse -> faster features; shared vocabulary -> fewer meetings; easier testing -> higher quality
  faster, accessibility reduces lawsuit risk; living foundation -> A/B and performance lessons roll
  in). Goal: a concrete commitment of real time and money.
- **Show, don't tell:** "make them feel the pain" with an interface inventory (principle 15).

## 15. Interface inventory (ch. 4)

"A comprehensive collection of the bits and pieces that make up your user interface" — screenshots of
one instance of each unique pattern, categorized. Full procedure, categories, timing (30-90 minutes),
and templates in interface-inventory.md. Benefits: captures all patterns and inconsistencies; gets
organizational buy-in ("You don't need to be a designer to recognize that having 37 unique button
styles probably isn't a good idea"); establishes scope of work; lays the groundwork and vocabulary for
the system.

## 16. Ask forgiveness, not permission; the Lego pile (ch. 4)

- If stakeholders still say no: "Do it anyways." Build design systems by default, like performance,
  accessibility and responsiveness. "When you give stakeholders the option to say no to something, they
  will. So simply don't give them that opportunity."
- Wolfram Nagel's Lego analogy: dump the bricks and rummage (gaze fixed on the final product) vs take
  time to organize the parts first — not visible in the final product, but produces "better work in a
  shorter amount of time".
- Stakeholders only need to see progress on the final product; after a successful launch, "pull back
  the curtain" and parlay the success into an official initiative. Preferable to get their blessing,
  but follow the craft's best practices even under resistance.

## 17. Redefining design beyond aesthetics; death to the waterfall (ch. 4)

- (Re)set expectations: "This is how we've always done things" is ludicrous in a 25-year-old industry.
- Print design focuses on visual aesthetics; the web adds speed, screen size, environment, technical
  capability, form factor, ergonomics, usability, accessibility, context, user preferences. Dan Mall:
  "we sell websites like paintings. Instead, we should be selling beautiful and easy access to content,
  agnostic of device, screen size, or context."
- Beyond looking good, design systems should: be accessible and resilient (inclusive); have flexible
  layouts and components; treat performance as a design principle; progressively enhance; be
  future-friendly. (Also ergonomics, input type, Section 508, legibility.)
- **Waterfall** (UX PDF -> visual comps -> "homepage_v9_final_for-review_FINAL_bradEdits_for-handoff.psd"
  slipped under the Code Cave door with "three weeks, out of budget") yields seven typefaces, nine
  button styles, desktop-only layouts, improbable content, invented hover/active/disabled states, and
  bruised relationships. Waterfall suits print and architecture where mistakes are costly; "Pixels are
  cheap." Work in parallel; research and IA tend to come earlier but must not block others; no
  discipline "fades away" — everyone keeps consulting until launch.

## 18. Development is design; the front-end prep chef (ch. 4)

- HTML and CSS are not programming languages; front-end builds the very UI designers craft, so "treat
  front-end development as a core part of the design process". Separating designers from front-end
  developers is "an absolutely terrible idea".
- Static pictures let stakeholders sign off only on pictures. Getting into the browser early confronts
  them with: flexibility, network impact, interaction, motion, ergonomics, colour/text rendering, pixel
  density, scrolling performance, device/browser quirks, user preferences — and kick-starts the pattern
  library. Not "design entirely in the browser": right tool at the right time; a static image and a
  working prototype can show the same idea simultaneously.
- **Prep chef:** "If developers aren't coding from day one of the project, there's something wrong with
  the process." Before any design exists: set up Git, dev servers, CMS, tooling; stub shell templates
  (header, footer, main) and anticipated patterns (e-commerce: site search, cart table, product detail
  placeholder, homepage, checkout; online service: sign-up/login, forgot password, dashboard). Crude
  markup is "a crucial starting point for collaboration and iteration"; developers then help validate UX
  decisions and teach source order and layout.

## 19. Iteration as subtractive sculpture; establishing direction (ch. 4)

- A digital process is like stone sculpture: rough the whole shape, then detail sections (face, arms,
  legs), stepping back regularly; fidelity builds over many passes ("we have the power of undo").
  Stakeholders must get comfortable reviewing works in progress; "rolling updates are preferable to
  big reveals"; communicate progress, not "a false sense of perfection".
- Agree on overall direction and "paint the broad strokes first" before high-fidelity work:
  - *UX:* lo-fi, mobile-first sketches; a bulleted list; "Do we have the right things on this screen?
    Are they in the right general order?"; gestural site-wide display patterns ("featured island",
    Jennifer Brook) with no layout/aesthetic/functional assumptions; or simply a spreadsheet of
    display patterns, content patterns, hierarchy and role per template (leftmost column read top to
    bottom = the mobile-first view).
  - *Visual:* 20-second gut test, style tiles, element collages (playbook.md).
  - *Front-end:* dependencies, shell templates, structural markup.
  Concurrent, not isolated. Jason Santa Maria: "Ideas are meant to be ugly." Any medium works (napkin,
  CodePen, Sketch, Balsamiq, After Effects).

## 20. Comps as hypotheses; deciding in the browser (ch. 4)

- Client feedback "it's like you're asking me to comment on how beautiful a face is by showing me the
  nose" means they are ready for context: create a full comp (TechCrunch article template) only after
  element collages resonate, to limit wasted effort. "The trick is knowing when to paint those full
  pictures, and knowing how long to dwell in static design documents."
- Read the feedback: "This feels all wrong" -> new comp. "Can we move this from here to here? Add a
  gray border? Increase the image size?" -> direction is good; fix in the browser.
- Static comps are "merely hypotheses rather than set-in-stone specifications. Only when transferred
  to the browser can any design hypothesis truly be confirmed or rejected." Dan Mall: "deciding in the
  browser." Once in the browser, stay there; designers react and make **spot comps** to iron out
  responsive wrinkles at the organism level. As each pattern matures, every template that includes it
  matures; new templates become "mostly ... stitching together existing patterns".

## 21. Artifact vs product; design-system-first; friendly friction (ch. 5)

- Nathan Curtis: "A style guide is an artifact of design process. A design system is a living, funded
  product with a roadmap & backlog, serving an ecosystem." And: "A system isn't a project with an end,
  it's the origin story of a living and evolving product that'll serve other products."
- If live products are the sole focus and the library is an offshoot, the library "snaps off and slides
  into the abyss": once it stops reflecting the products it becomes obsolete and maintenance "devolves
  into a smattering of hotfixes and ad hoc changes".
- **Design-system-first** adds "friendly friction": consider how every improvement, request or feature
  affects the whole system. Example: an A/B test shows a custom-styled dropdown underperforms the
  browser default on the product detail page; instead of fixing that one page, ask whether it fails
  elsewhere and modify the dropdown pattern globally. "Broken behavior and opportunities to enhance the
  UI will often be realized at the application level, but those changes should often be acted on at
  the system level."
- Redefine "done": the web is never done; project-based work "set[s] it, forget[s] it, then move[s] on".

## 22. Makers and users; team makeup (ch. 5)

- **Makers** create, maintain and govern; bird's-eye view. **Users** apply patterns to specific
  applications; on-the-ground view. "Not everyone in the organization needs to contribute directly ...
  but someone (or more likely, some people) must take ownership of it." Jina Bolton: "The Design System
  informs our Product Design. Our Product Design informs the Design System."
- Sizing: Salesforce's team is about a dozen full-time employees serving thousands of users — dedicate
  "at least a few" FTEs at that scale. Small orgs: a hat worn by senior staff with the experience to
  decide and the authority to enforce. Third parties: limited influence (the system must enter the
  organization's DNA) but valuable perspective; "teach them to fish".
- Users may be the same team, other product teams, juniors, agencies or external shops; the further
  apart, the more documentation matters. A system "scales best practices" so users "don't have to be
  senior-level ... to produce good work" — it is a quality-control vehicle.
- Hands on the work: UX designers, visual designers, front-end developers. Consulted: back-end
  engineers (architecture affecting the front-end), executives (initiatives), users (application needs).

## 23. Governance and the three types of pattern change (ch. 5)

- Misconception: the system is "an omnipotent and unchangeable source of truth"; rigid systems make
  users feel "handcuffed" and they look elsewhere. Count on change.
- Governance questions and communication rituals: see maintenance-governance.md.
- Change types (Canonical's Vanilla team drew a decision tree from proposal to acceptance):
  - **Modification** — features, bug fixes, visual tweaks, performance, accessibility, refactoring, UX
    best-practice updates. Keep patterns fresh (no "Web 2.0-looking ... bevels and crusty code").
  - **Addition** — gaps emerge as more products use the system. "If every whim results in a brand new
    pattern, the design system will become a bloated and unwieldy Wild West." Ask: one-off or
    leverageable? Assume one-off until another team says "I want that!"
  - **Removal** — a pattern proved a terrible idea, the industry moved on, it sat unused, or users
    complained. Deprecate without "pulling the rug": Salesforce's Sass Deprecate flags patterns headed
    for removal and recommends alternatives.

## 24. The holy grail and its technical bridges (ch. 5)

- Alex Schleifer (Airbnb): "The biggest existential threat to any system is neglect." Systems decay
  when updating patterns, docs and apps is too hard; reducing that friction is a top priority.
- **Holy grail:** pattern library and live applications perfectly in sync — change a pattern once and
  both update (Lonely Planet's Rizzo: an API for UI patterns consumed by production and the library).
- Spectrum (Marcelo Somers, "Chasing the Holy Grail"): manual copy-paste at one end, library baked
  into production at the other. Sharing CSS and presentational JS is relatively easy (compiled files on
  a CDN with a versioned URL, e.g. `http://mycdn.com/1.3.5/styles.css`; upgrading = bump the version).
  Sharing markup is hard because it is intertwined with back-end logic; bridge it with a templating
  language used on both sides (Mustache, Handlebars, Twig, Underscore, Jade, Nunjucks). Phase2: Pattern
  Lab + Drupal both speak Twig; the Component Libraries module includes the same templates "without any
  template duplication".
- Culture check: many platforms/technologies, a scattered multinational, a highly decentralized
  culture, or a federal government (Draft U.S. Web Design Standards distributes downloadable markup
  and styles instead) may not be grail-compatible. Even "a handful of go-to UI patterns, some helpful
  documentation, and guiding principles" point toward it; crawl before you run.

## 25. The ten "make it ..." maintenance principles (ch. 5)

Frost's closing list, verbatim in spirit:
1. **Official** — allocate real time, money and resources (path: make a thing -> show it's useful ->
   make it official).
2. **Adaptable** — count on change; clear governance plan.
3. **Maintainable** — seek the holy grail; make deploying and communicating changes easy.
4. **Cross-disciplinary** — a watering hole the whole organization gathers around (the carousel needs
   business owners, editorial, copywriters, art directors, UX, front-end, back-end).
5. **Approachable** — attractive, easy-to-use guide with helpful documentation (Yelp's front page says
   what it is, who it's for, how to use it). Don't let "Big, Official Thing" ambitions stop you starting.
6. **Visible** — communicate change (change logs, roadmap, success stories, tips), evangelize (internal
   blog, channel) from before launch, train and support, and make it public ("These are UI patterns,
   not nuclear codes"; public guides add accountability and recruit — Jina Bolton joined Salesforce
   after seeing theirs).
7. **Bigger** — include brand, voice and tone, code, design principles, writing guidelines; native
   iOS/Android patterns beside web (Intuit Harmony).
8. **Agnostic** — name patterns by structure, not context or content ("carousel" not "homepage
   carousel"; "card" not "product card"; blur the content when naming).
9. **Contextual** — show what a pattern is made of and where it is used (lineage; screenshots/videos
   as in material design).
10. **Last** — a solid foundation for years; value grows like wine, not a car off the lot; even a
    rebuild still needs buttons, form fields and tabs.

Details and checklists: maintenance-governance.md.
