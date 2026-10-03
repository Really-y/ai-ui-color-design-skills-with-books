# Principles and concepts (Garrett, *The Elements of User Experience*, 2nd ed.)

Each entry: name, the author's definition, why it matters, how to apply, pitfalls. Chapter references
in parentheses. Grouped by plane, with the framework itself first.

## Table of contents

1. The framework (ch. 1-2): user experience, user-centered design, five planes, ripple effect,
   the scheduling rule, the duality, element map, content and technology
2. Strategy plane (ch. 3): product objectives, brand identity, success metrics, user needs,
   segmentation, research methods, usability, personas, stakeholders, strategy document
3. Scope plane (ch. 4): why define scope, feature, functional specs vs requirements, content
   requirements, three categories of requests, scenarios, writing rules, prioritization, feasibility
4. Structure plane (ch. 5): interaction design, conceptual models, error handling, information
   architecture, top-down/bottom-up, nodes, four structures, organizing principles, facets,
   nomenclature, controlled vocabulary, thesaurus, metadata, architecture diagram
5. Skeleton plane (ch. 6): interface/navigation/information design, convention, metaphor,
   interface elements, navigation goals and types, wayfinding, wireframes
6. Surface plane (ch. 7): sensory design, follow the eye, contrast, uniformity, grid, consistency,
   color, typography, design comp, style guide
7. Applying the elements (ch. 8): problem location, consequences, three unconscious design modes,
   "why did you do it that way", testing's role, marathon vs sprint

---

## 1. The framework (ch. 1-2)

### User experience
- **Definition:** the experience a product creates for the people who use it in the real world; how it
  works "on the outside", where a person comes into contact with it, not its inner workings (ch. 1).
  Questions it answers: Is it hard to do simple things? Is it easy to figure out? How does it feel?
- **Why:** every product used by someone creates an experience (books, ketchup bottles, armchairs).
  Little things decide outcomes: a power button with no click/light/resistance means no coffee, which
  means a lost customer (ch. 1).
- **Apply:** when evaluating, separate aesthetic design (shape, texture), functional design (it triggers
  the right action) and UX design (does the button work in the context of the rest of the product and
  of what the user is trying to do: "Is it too small for such an important function? Is it in the right
  place relative to the other controls used at the same time?") (ch. 1).
- **Pitfall:** "form follows function" is fine for concealed internals; for user-facing parts the
  correct form is dictated by users' psychology and behavior (ch. 1).

### Complexity multiplies failure points
- Simple products (chair, table) have UX requirements built into their definition. For complex
  products (a phone) the UX requirements are independent of the definition, and each extra feature,
  function or step is one more chance for the experience to fall short (ch. 1).

### Self-service and self-blame
- Web sites (and most digital products) are self-service: no manual, no training, no representative.
  When users struggle they blame themselves and feel stupid; nothing drives people away faster (ch. 1).
- "Featuritis": more features is only a temporary advantage and makes the product unwieldy for the
  very newcomers it was meant to attract (ch. 1).

### Good UX is good business
- Bad experience: they don't come back; OK experience but a better one at a competitor: they go there.
  UX affects loyalty more than features or brand messaging; "you don't get much of a second chance" (ch. 1).
- ROI via **conversion rate** (percentage of users who take the next step): worked example 3 sign-ups /
  36 visitors = 8.33%. A change as small as one-tenth of one percent in conversion can mean a revenue
  increase of ten percent or more. Conversion is a better UX measure than raw sales, which also depend
  on marketing (ch. 1).
- Internal tools: UX improves efficiency in two forms, working faster and making fewer mistakes, plus
  job satisfaction, retention, lower recruiting/training cost (ch. 1).

### User-centered design
- **Definition:** take the user into account every step of the way; everything the user experiences
  should be the result of a conscious decision. Compromises for time/cost are allowed, but a UCD
  process ensures they don't happen by accident (ch. 1).

### The five planes
- Bottom to top: **strategy, scope, structure, skeleton, surface**; each plane is less abstract and
  more concrete than the one below (ch. 2).
  - Surface: the pages/screens of images and text; some images clickable, some illustrative.
  - Skeleton: placement of buttons, controls, photos and text blocks, arranged for maximum effect and
    efficiency (remember the logo, find the cart button).
  - Structure: how users got to a page and where they can go next; what the categories are.
  - Scope: which features and functions exist at all (e.g. saved shipping addresses).
  - Strategy: what the organization wants from the product and what users want from it.
- Each plane depends on the planes below. Misalignment derails projects, misses deadlines, inflates
  cost, and ships products users hate (ch. 2).

### Ripple effect
- Strategy decisions ripple up through every plane; the choices available on each plane are
  constrained by decisions on the planes below. Choosing an "out of bounds" option on an upper plane
  forces rethinking lower planes. Dependencies run in both directions: upper-plane work can force a
  re-evaluation (or a first evaluation) of lower-plane issues (ch. 2).
- Inputs for decisions on every plane: what the competition does, industry best practice, what you
  know about users, common sense (ch. 2).

### The scheduling (ripple) rule
- Waterfall (finish each plane before starting the next) gives unsatisfactory results. Treating
  lower-plane decisions as set in stone jeopardizes the schedule and the product.
- **Rule:** plan so that work on any plane cannot *finish* before work on the planes below has finished.
  "Don't build the roof before you know the shape of the foundation" (ch. 2).

### The basic duality
- The Web (and most products) is both a platform for **functionality** (tasks, steps, product as a
  tool) and an **information medium** (what information is offered, what it means; help people find,
  absorb, make sense). Historically two communities (software/application people vs publishing/
  library-science people) used different vocabularies; most products are hybrids (ch. 2).

### Element map
| Plane | Functionality side | Information side |
|---|---|---|
| Strategy | user needs + product objectives (shared) | |
| Scope | functional specifications: detailed description of the feature set | content requirements: description of required content elements |
| Structure | interaction design: how the system behaves in response to the user | information architecture: arrangement of content elements to facilitate understanding |
| Skeleton | interface design: arranging interface elements so users can interact with functionality; plus information design (shared): presenting information so it is understood | navigation design: screen elements that let users move through the IA; plus information design |
| Surface | sensory design (shared) | |
(ch. 2)

### Using the elements
- Lines blur; some problems straddle elements; within a plane the elements work together (information,
  navigation and interface design jointly define the skeleton). Titles like "information architect"
  don't matter; someone just has to spend part of their time thinking about each issue (ch. 2).
- Two shaping factors not treated as elements: **content** ("content is king"; users don't visit for
  the joy of navigation; can you obtain, catalog, maintain it?) and **technology** (determines what
  experience is possible) (ch. 2).

---

## 2. Strategy plane (ch. 3)

### The two root questions
- What do we want to get out of this product? What do our users want to get out of it? Not answering
  them before code, pixels or servers is the most common reason products fail. The key word is
  **explicit**: the more clearly both are articulated, the more precisely choices can be tuned (ch. 3).

### Product objectives
- **Definition:** the organization's internal objectives for the product. Garrett prefers this term
  over "business goals/drivers": too narrow (not every organization has business goals) and too broad
  (we want what the *product* must accomplish specifically) (ch. 3).
- **Calibration:** too general ("make money / save money"); too specific = a solution ("provide a
  real-time text communications tool" explains neither how it helps the organization nor the user).
  Define the conditions for success without defining the path; don't jump to solutions before
  understanding problems (ch. 3).
- **Pitfall:** objectives that exist only as unspoken understanding; different people then hold
  different ideas of what the product is for.

### Brand identity
- **Definition:** a set of conceptual associations or emotional reactions; it is inescapable: users'
  interactions with the product create an impression of the organization whether you plan it or not.
  Visual branding (logos, palettes, type) is only part of it (ch. 3).
- **Apply:** codify the specific qualities of the intended impression as an explicit product objective.
  Applies to nonprofits, government agencies and individuals too.

### Success metrics
- **Definition:** indicators tracked after launch to see whether the product meets objectives and user
  needs; they also prove UX value to skeptical budget holders (ch. 3).
- **Examples:** time per visit (raise it if you want exploration, lower it for get-in-get-out tasks);
  visits per registered user per month vs a target line; ad impressions; indirect metrics: fewer
  support calls, faster sales cycles from an intranet (ch. 3).
- **Rules:** a metric must be tied to user behavior that design choices can shape; UX cannot bring new
  users (marketing does) but strongly affects return visits; long-term changes are hard to attribute;
  any metric viewed in isolation misleads (competitor campaigns, bad press), so look beyond the site.
- **Pitfall:** optimizing a metric against users (navigation layers to raise impressions): short-term
  gain, then users leave and impressions fall below where they started.

### User needs
- Goals for the product that come from outside the organization. We are not designing for ourselves
  or an idealized user like us; define who users are, research them (ask questions, observe behavior),
  then define and prioritize needs (ch. 3).

### User segmentation
- Divide the audience into groups sharing key characteristics. Approaches: demographic (gender, age,
  education, marital status, income; general "men 18-49" or specific "unmarried, college-educated women
  25-34 earning over $50,000"); psychographic (attitudes/perceptions about the world or the subject);
  attitude toward technology (hours per week online, part of daily life?, enjoys tech?, latest gadgets
  vs upgrade only when forced; technophobes vs power users); subject-matter expertise (novice vs
  professional cooks; new vs seasoned investors); social/professional role (student vs parent) (ch. 3).
- **Rules:** revise segments after research (split 25-29 vs 30-34 if needs differ; merge 18-24 with
  25-34 if similar). You need only as many segments as there are distinct sets of needs. Needs can be
  in direct opposition (novices: simple step sequence; experts: unified rapid-access interface); you
  cannot satisfy both with one solution, so either focus on one segment or build two separate ways to
  do the task; this strategic decision has consequences everywhere (ch. 3).

### User research methods
- Surveys, interviews, focus groups: general attitudes and perceptions; articulate beforehand what you
  need to learn (what they do vs why).
- User tests, field studies: specific behavior with the product.
- Trade-off: more time per user = more detail but fewer users.
- **Contextual inquiry:** the most powerful, comprehensive toolkit (from anthropology); time-consuming
  and expensive; lightweight variants exist but go less deep.
- **Task analysis:** every interaction happens inside a task (focused: buy movie tickets; broad: learn
  international commerce regulations); examine the precise steps via interviews (stories) or field
  observation.
- **User testing:** the most common method; "not testing your users, users test what you've produced";
  on finished products (before a redesign, or to catch issues before launch), works in progress, or
  prototypes (paper sketches, lo-fi mockups, click-through prototypes; different kinds at different
  stages). Scope can be narrow (task completion) or broad (does the redesign reinforce or undermine the
  brand?). Have a clear sense of what to investigate before sitting down with users.
- **Card sorting:** index cards each naming/describing/picturing a content item; users sort into
  natural groups; analyze across several users to learn how they categorize information (ch. 3).

### Usability
- Many definitions; all share one core: users need usable products: "the most universal user need of
  all" (ch. 3).

### Personas (user models, user profiles)
- **Definition:** a fictional character constructed to represent the needs of a whole range of real
  users; consistent with research, but specific details are invented to breathe life into it (ch. 3).
- **Apply:** give a name and stock photo; print and post; ask in decisions "Would that work for Janet?
  How would Frank react?" Typical fields (from the book's Janet/Frank sheets): quote, age, occupation,
  family, household income, technical profile (comfort, device, connection, hours online), internet use
  (where, for what), favourite sites.

### Team roles: stakeholders and rank-and-file
- Strategists are often the first line item cut. **Stakeholders:** senior decision-makers responsible for
  parts of the organization affected by the product (e.g. marketing communications, customer service,
  product managers). **Rank and file:** day-to-day staff, often neglected, who know what customers
  struggle with better than managers do; customer feedback rarely reaches product teams (ch. 3).

### Strategy (vision) document
- Not just a list: an analysis of relationships among objectives and their fit with the organization,
  supported by quotes from stakeholders, rank-and-file and users. Keep it concise (people won't wade
  through hundreds of pages). Worst mistake: restricting the team's access; designers, developers and
  project managers all need it. Strategy should evolve and be refined systematically, while avoiding a
  moving target (ch. 3).

---

## 3. Scope plane (ch. 4)

### Why define scope
- Defining scope is a valuable *process* (forces conflicts and rough spots into the open while the
  product is hypothetical; sorts now vs later) and a valuable *product* (reference point and common
  language for the team). It "drives ambiguity out of the design process" (ch. 4).
- **Reason #1, know what you're building:** ends the "Telephone" game of word-of-mouth impressions and
  the trap where everyone assumes someone else owns a crucial part; lets you parcel out responsibility
  and see overlaps (support documentation and product spec sheets turned out to belong to one group).
- **Reason #2, know what you're not building (right now):** a framework for evaluating ideas that arrive
  mid-project; stockpile good ones for the next milestone (v1.0 now, v1.1 later). Unmanaged
  requirements become **scope creep**, a snowball rolling downhill.

### Strategy asks why, scope asks what
- Strategy: "Why are we making this product?" Scope: "What are we going to make?" (ch. 4)

### Feature
- Garrett uses "feature" for both software functions and content offerings; the two are defined in
  very similar ways (ch. 4).

### Functional specifications vs requirements
- Some organizations distinguish requirements (start: what it should do) from specifications (end:
  what it actually does); mostly interchangeable. In the book: "functional specifications" = the
  document, "requirements" = its contents (ch. 4).
- Specs have a bad reputation (dull, unread, out of date), a self-fulfilling prophecy. Things changing
  in implementation is not a reason to abandon specs; make the process lightweight so the spec doesn't
  become a separate project. "Documentation won't solve your problems. Definition will." Clarity and
  accuracy, not volume; only what needs definition to avoid confusion; only decisions actually made.

### Mutual implications of content and functionality
- Content requirements imply functionality: a CMS must handle the languages/data formats, the approval
  workflow (six executive VPs and a lawyer), dynamic recombination per user or device.
- Functional requirements imply content: instructions on configuration screens, error messages. The
  placeholder "Null input field exception" ships when nobody made error messages a content requirement.
  Have someone look at the application "with an eye toward content" (ch. 4).

### Requirement types and level of detail
- Product-wide requirements (branding; technical such as supported browsers/OS) vs feature-specific
  ones. Detail depends on the project: a complex subsystem may need high detail; a mass of
  homogeneous PDFs needs only general content requirements (ch. 4).
- Hardware constraints (camera? GPS? gyroscopic sensors?) inform and constrain the feature set.

### Sources and the three categories of requests
- Most productive source: users; most common: stakeholders. Ask them (reuse ch. 3 research methods).
- (1) Things people say they want (some are good). (2) Things they say they want but don't actually
  want: imagined solutions that are unworkable or treat a symptom; explore them to find the real
  requirement. (3) Features they don't know they want: emerge from brainstorming around strategic
  objectives. Insiders can be least able to imagine new directions (they forget which constraints are
  real vs historical); cross-functional brainstorms (engineer + customer-service agent + marketer) open
  minds (ch. 4).
- Other generators: remove impediments (a user who already decided to buy: what makes selecting and
  buying easier?); **scenarios** (short narratives of a persona pursuing a need); competitors (same
  needs and objectives; how did they handle the trade-offs?) and non-competitors (gaming platforms'
  social groups as inspiration for a DVR).

### Writing requirements
- **Be positive:** state what the system does to prevent the bad thing, not the prohibition.
- **Be specific:** leave as little as possible to interpretation; it's the only way to tell whether a
  requirement was met.
- **Avoid subjective language; requirements must be falsifiable:** it must be possible to show when one
  has not been met. Replace taste words with references to criteria (branding guidelines document).
- **Quantify** when possible ("at least 1,000 simultaneous users" instead of "high performance") (ch. 4).

### Content requirements
- Content = text, images, audio, video; types combine to fulfil one requirement (article + photos +
  clips). Identify all types per feature to see resource needs or whether it can be produced at all.
- Format vs purpose: "We should have FAQs" names a format; the purpose is ready access to commonly
  needed information, which other content could fulfil; FAQs typically neglect "frequently".
- Record a rough size per feature (word count; pixel dimensions; file size for audio/PDF); thumbnails
  vs full-screen photos change the design.
- Identify an owner for each content element as early as possible; otherwise loved-when-hypothetical
  features become gaping holes. Content needs constant maintenance; "post and forget" degrades.
- Set an update frequency per feature from objectives (how often do we want users back?) and needs (how
  often do they expect updates?), compromised with resources.
- Record the intended audience per piece (children vs parents vs both need three approaches).
- For existing content, build a **content inventory** (a large, tedious spreadsheet) so everyone knows
  what there is to work with (ch. 4).

### Prioritizing requirements
- Objectives and requirements rarely map one-to-one (one requirement may serve several objectives; one
  objective may need several requirements).
- Evaluate against product objectives, user needs, and **feasibility**: technically impossible (smell
  over the Web), resource-infeasible (people/money, especially content), time-infeasible (three months
  of work, launch in two: push to a later release). Technology or organizational change can sometimes,
  not always, lift resource constraints; impossible stays impossible.
- Features conflict; trade-offs are decided by strategic objectives (one-step ordering vs legacy
  databases: multi-step flow or rework the database?).
- Out-of-scope but feasible, good ideas may signal a strategy shift; reexamine objectives. If you
  revisit many aspects of strategy, requirements started too early.
- A priority hierarchy among objectives in the vision document is the primary ranking factor; without
  it, politics decides. Stakeholders start with features and must be coaxed back to strategy; features
  acquire champions. Resolve by appealing to the defined strategy: focus on goals, not means; show the
  champion that her goal can be met another way; empathy is essential (ch. 4).

---

## 4. Structure plane (ch. 5)

### Structure
- Defines how the pieces fit together into a cohesive whole; the first plane with tangible influence,
  but the decisions are still conceptual (ch. 5).

### Interaction design
- Describes possible user behavior and defines how the system accommodates and responds to it; a
  "dance" in which each partner anticipates the other. Once lumped under interface design. Software was
  historically built for what was technically efficient (programmers care about what it does and how),
  and "computer literacy" was the proposed remedy; the approach that works best for the technology is
  almost never the one that works best for the person (ch. 5).
- Both ID and IA define patterns and sequences in which options are presented: ID for performing and
  completing tasks, IA for conveying information. Neither is about technology; both are about how
  people behave and think.

### Conceptual models
- Users' impressions of how interactive components will behave: is a feature a thing consumed, a place
  visited, or an object acquired? What matters is consistency, not which model (ch. 5).
- Shopping cart = container model: "put things into / take out of", add and remove functions,
  checkout. Alternative: catalog order form: an edit function replaces add/remove; users "send in" an
  order. The retail-store model is now a convention; if your users shop elsewhere, keep it. Breaking
  convention needs a good reason and an alternate model users can correctly interpret.
- Models can cover one component or the whole system (Slate's magazine model with front, back, page
  numbers and "turn the page"; it didn't translate to the Web and was dropped).
- Don't explain the model to users (can confuse); apply it consistently during design; learn the
  models users bring; ideally users pick it up because behavior matches implicit expectations.
- Don't take metaphors literally (old Southwest Airlines home page: a picture of a service desk with
  brochures and a telephone; a reservation resembles a phone call, but the system needn't be a phone).

### Error handling (layers: prevention, correction, recovery)
1. Best defense: make the error impossible (automatic-transmission cars won't start in gear).
2. Next: make the error difficult.
3. Help users recognize and fix errors (helpful messages, easy-to-interpret interfaces); the system may
   fix errors itself, but well-intentioned auto-correction is among the most irritating software
   behavior (Word's corrections get switched off).
4. Some actions don't look like errors until too late: provide recovery (undo and other forms).
5. Unrecoverable errors: plenty of warning, effective only if noticed. Too many "Are you sure?"
   confirmations make the important one get overlooked and annoy more users than they help (ch. 5).
- Each layer raises the share of users who end with a positive experience.

### Information architecture
- An old practice (as old as communication) concerned with how people cognitively process information;
  relevant to any product where users must make sense of information, including functionality-heavy
  ones (a mobile phone). On content sites: organizational and navigational schemes to move through
  content efficiently; related to information retrieval; often must also educate, inform or persuade.
  Core task: categorization schemes matching objectives, user needs and content (ch. 5).

### Top-down vs bottom-up
- Top-down: from strategy (objectives + needs): broadest categories, then logical subsections: an empty
  shell to slot content into. Risk: overlooks important details of the content itself.
- Bottom-up: from scope (content and functional requirements): group existing/planned material into
  low-level then higher-level categories. Risk: so tuned to current content it can't accommodate
  change. Neither is better; balance both (ch. 5).

### Steps vs sense
- No fixed number of categories per level; categories just have to be right for users. Counting steps
  or clicks is not the measure of quality; what matters is whether each step made sense and followed
  naturally. Users prefer a clearly defined seven-step process to a confusingly compressed three-step
  one (ch. 5).

### Adaptability
- Sites are living entities; an effective structure accommodates growth (new content within a section,
  entirely new sections). Accumulated content eventually forces revisiting organizing principles
  (press releases day-by-day works for months; by topic after years). If objectives or needs change,
  rework the structure; the need rarely announces itself, and by the time you notice, users are already
  suffering (ch. 5).

### Nodes
- The basic unit of information structure: any piece or group of information from a single price to an
  entire library. Using nodes (not pages/documents/components) gives a common language and lets you set
  the level of detail explicitly: page as base node (most projects), or section, or elements within a
  page (ch. 5).

### The four structure classes
- **Hierarchical (tree, hub-and-spoke):** parent/child; children are narrower concepts; every node has
  a parent up to the root. Well understood by users and natural to software; by far the most common.
- **Matrix:** move along two or more dimensions; lets users with different needs (browse by color vs by
  size) navigate the same content. More than three dimensions as primary navigation causes problems;
  the brain can't visualize movement in four or more.
- **Organic:** no consistent pattern; case-by-case connections; no strong sections. Good for exploring
  topics whose relationships are unclear or evolving and for free-form exploration (entertainment,
  education); weak sense of location; hard to find the same content again.
- **Sequential:** offline media's structure (books, articles, audio, video); language itself. On the
  Web used mostly at small scale (an article, a section); large-scale only when order is essential
  (instructional material) (ch. 5).

### Organizing principles
- The criterion deciding which nodes are grouped and which separated; varies by area and level.
  Examples: audience (Consumer / Business / Investor), geography (North America / Europe / Africa),
  chronology (news: timeliness matters most to users and creators), then content-tied at the next level
  (Baseball / Tennis / Hockey; International / National / Local). Top levels follow objectives and user
  needs; lower levels follow content and functional requirements (ch. 5).
- Every collection has an inherent structure, usually more than one; the challenge is the *right* one.
  A car database ordered by weight is wrong for consumers (make, model, type) and right for overseas
  shippers.

### Facets
- Library-science term for attributes usable as organizing principles; simple and flexible, but the
  wrong facets are worse than none. Exposing every facet and letting users choose creates an unwieldy
  mess unless the information is very simple. The burden of choosing what is foremost in users' minds
  is on the designer, not the user (ch. 5).

### Nomenclature, controlled vocabulary, thesaurus
- **Nomenclature:** descriptions, labels and terminology. Use the users' language, consistently.
- **Controlled vocabulary:** a set of standard terms for the product; built from user research; keeps
  internal jargon off the site; gives distributed content producers one definitive resource.
- **Thesaurus:** also documents common but non-approved terms (jargon, shorthand, slang, acronyms)
  mapped to approved ones, plus broader/narrower/related relationships; reveals the range of concepts
  and can suggest new architectural approaches (ch. 5).

### Metadata
- "Information about information": a structured description of a content piece. Example for an
  article about a product used by volunteer fire departments: author, date posted, type of piece (case
  study/article), product name, product type, customer industry, related topics (municipal agencies,
  emergency services). More metadata = more structural flexibility (spin up an "emergency services"
  section from existing content). Requires consistent terms (controlled vocabulary) to power automation
  such as dynamic topic links. Search engines are "very, very dumb" string matchers; connecting them to
  a thesaurus and metadata maps a disallowed term to the preferred one and returns targeted results
  plus related recommendations instead of nothing (ch. 5).

### Architecture diagram
- The major documentation tool (text outlines for simple hierarchies; spreadsheets/databases for very
  complex ones). Called "architecture diagram", not "site map" (which is a user-facing navigation
  tool). Don't document every link; document conceptual relationships: which categories go together,
  how the steps of an interaction sequence fit. Garrett's Visual Vocabulary (2000) is a standard shape
  set for this (ch. 5).

### Who owns structure
- Often lands somewhere by default (editorial/marketing in content-led organizations; the technical
  project manager in tech-led ones). Titles: interaction designer, information architect, user
  experience designer. A full-time specialist pays off with a steady stream of new content and
  functionality, not for maintenance-only operations between redesigns. The product will have a
  structure whether or not it is planned; planned ones need fewer overhauls (ch. 5).

---

## 5. Skeleton plane (ch. 6)

### Skeleton
- Structure defines how the product works; skeleton defines what form that functionality takes, at the
  scale of individual components and their relationships (ch. 6).

### The three elements and how to sort a problem
- Ability to **do** things: interface design (the means by which users contact the functionality).
- Ability to **go** places: navigation design (the lens through which users see the IA and move
  through it).
- **Communicating** ideas: information design (the broadest; crosses both sides; neither interface nor
  navigation design can fully succeed without it). "Good navigation design can't correct bad
  information design." Naming the problem type is how you know whether you solved it (ch. 6).

### Convention
- Habit and reflex underpin interaction; convention lets reflexes transfer between products. Garrett's
  car with nonstandard controls made friends wash the windshield when they wanted headlights. A
  nonstandard phone keypad might cost about three seconds per call, each filled with frustration. The
  3x4 phone pad spread to microwaves and remotes; the "10-key" layout (inverted digits) rules
  calculators, keyboards, ATMs, registers; both are 3x4 so people adapt, though one standard would be
  best (ch. 6).
- **Rule:** not slavish adherence; be cautious about deviating and do so only when a different approach
  offers clear benefits; have explicit reasons for every choice.
- Internal consistency outranks consistency with other products: features sharing a conceptual model
  share interface conventions; cross-cutting concepts (start, finish, go back, save) get the same
  treatment everywhere.

### Metaphor
- Building a product around concrete metaphors is "cute and fun" but almost never works as well as it
  seems; often not at all. Real-world interfaces are products of physical constraints that screens
  don't have. A metaphor is only one of many associations a user might make (a telephone icon: call?
  voicemail? pay the bill?), especially across cultures; some users always guess wrong; eliminate the
  guesswork. Acceptable when it reduces mental effort (phone-book icon for a directory); problematic
  otherwise (coffee-shop picture for a chat area) (ch. 6).

### Interface design
- Select the right elements for the task and arrange them to be readily understood and easily used.
  Which functions land on which screens is interaction design (structure); how they are realized is
  interface design.
- Successful interfaces: users immediately notice the important stuff; unimportant stuff isn't
  noticed, sometimes because it isn't there. A major challenge is deciding what users don't need and
  reducing its visibility or omitting it.
- Programmers rightly treat edge cases as equal; interfaces must not: weight the most likely courses
  of action and make them easiest. Not just "make the likely button biggest": choose defaults from your
  understanding of tasks (leave "Show Me More Detail" checked if most users want detail); better still,
  remember last selections, though that can be technically costly (ch. 6).
- Technology constrains options: bad for innovation, good because a small set of standard controls is
  learned once. Conventions change slowly (gestural, touch).
- Standard elements: checkboxes (independent options), radio buttons (one of mutually exclusive),
  text fields, dropdown lists (radio behavior, compact, hides options), list boxes (checkbox behavior,
  compact, scroll), action buttons (take what the user entered and act). Trade-offs: dropdown saves
  space but hides choices; typing categories spares the database but loads the user; with six options
  checkboxes may be better. Technologies that don't enforce standard elements give more choices and
  are harder to get right.

### Navigation design: three simultaneous goals
1. Get users from one point to another (you can't link everything to everything; choose for real
   behavior; links must work).
2. Communicate the relationships among the navigation's own items (importance, differences).
3. Communicate the relationship between those items and the current page.
- Our physical sense of direction is useless in information space, so every page must say where the
  user is and where they can go. Whether users build mental maps is debated; assume they carry no
  knowledge from page to page (search engines make any page an entry point) (ch. 6).

### Navigation types
- **Global:** access to the broad sweep of the whole site; the key access points (nav bar to main
  sections). Not necessarily on every page, though that is a good idea. "Persistent" means appearing
  throughout; persistent is not the same as global.
- **Local:** what's nearby (parent, siblings, children); if the architecture reflects users' thinking,
  local navigation gets the most use.
- **Supplementary:** shortcuts to related content not reachable via global/local; gives some faceted
  benefits while keeping a hierarchy.
- **Contextual (inline):** links embedded in content; underused or misused; the moment of reading is
  the moment of need, so put the link there instead of making users scan or search. Too many links =
  clutter.
- **Courtesy:** items not needed regularly but handy (contact info, feedback forms, policies); like
  store hours posted at the entrance.
- **Remote navigation tools** (stand-alone; used when users give up on the other systems): **site map**
  (one-page hierarchical outline; top-level sections plus major second-level; no more than two levels,
  otherwise the high-level architecture is probably wrong); **index** (alphabetical topics with links;
  only for large, diverse content; per-section indexes for divergent audiences) (ch. 6).

### Information design
- Decisions on how to present information so people can use or understand it; the glue of the
  skeleton. Visual choices (pie vs bar chart; binoculars vs magnifying-glass icon) and grouping/
  arranging (contact fields in conventional order, then grouped into personal / address / other
  contact). Harder sets (power limit, rotor size, tank capacity...) must be grouped the way users think.
  This is micro-level IA, communicated on the page. Interfaces also communicate: error messages and
  instructional text are classic information design problems (the challenge is getting instructions
  read) (ch. 6).

### Wayfinding
- Helping people know where they are and where they can go; borrowed from public spaces (color-coded
  parking garages; airport signs and maps). Navigation design supplies the choices; information design
  supplies non-navigational cues: section color coding (almost never alone; it reinforces another
  system), icons, labeling systems, typography that say "you are here" (ch. 6).

### Wireframes (page schematics)
- Page layout is where information, interface and navigation design unite. A wireframe is a bare-bones
  depiction of all page components and how they fit; heavily annotated with pointers to architecture
  diagrams, requirements, existing content locations, and notes on behavior. The architecture diagram
  is the grand vision; the wireframe shows how it is fulfilled; sometimes supplemented by navigational
  specifications. One wireframe can template a small product; otherwise a small number of standard
  screens emerge (not one per screen). Everyone uses it: strategy/scope/structure people verify
  expectations; builders answer "how should this work". The dispute between UX designers (visual
  designers obscure architectures) and visual designers (reduced to paint-by-numbers) is resolved only
  by building wireframes together, which also surfaces problems early. Documentation is a means, not
  an end: pencil sketches with sticky notes suffice for a co-located pair; a formal document is needed
  for a programming team halfway around the world. Produce the right level "and not fooling yourself
  that you can get by with less" (ch. 6).

---

## 6. Surface plane (ch. 7)

### Sensory design
- Skeleton = arrangement; surface = sensory presentation of those arrangements. Senses: smell/taste
  rarely (food, fragrance; "new car smell" comes from materials); touch = industrial design (shape,
  texture, materials) plus vibration in phones and game controllers; hearing = informative beeps
  (headlights on, seat belt, key in ignition) and personality (TiVo's sounds); vision = where designers
  have the most sophistication (ch. 7).

### Evaluate by function, not taste
- Everyone's aesthetics differ, but decisions needn't be taste contests: ask how well the design
  supports the objectives of each lower plane. Does the look blur distinctions between sections
  (undermining structure) or clarify options (reinforcing it)? Brand identity through visuals is a
  strategy matter: a technical, authoritative identity is not comic-book fonts and pastels (ch. 7).

### Follow the eye
- Ask: where does the eye go first? Is that element important to strategic objectives or a
  distraction? Eyetracking for research; for fine-tuning, just ask people or yourself; squint, blur, or
  view from across the room to find the dominant element. Self-test by noticing unconscious eye
  movement; with others, have them call out elements in order of attention. Patterns are consistent;
  outliers probably aren't self-aware or are pleasing you. A successful pattern (1) flows smoothly
  ("busy"/"cluttered" = eyes bouncing among competing elements) and (2) gives a guided tour of the
  possibilities relevant to the current task without overwhelming detail or distracting from needed
  information and functions (ch. 7).

### Contrast
- The primary tool for attention; without it a design is a gray featureless mass. Contrast highlights
  essentials, shows relationships among navigation elements, and communicates conceptual groups in
  information design. Error messages blending into the page need contrast (red text, bold graphic).
  Differences must be large enough to read as intentional; similar-but-not-the-same makes users wonder
  "mistake? am I supposed to notice?". Overuse produces clutter (ch. 7).

### Uniformity and grid
- Uniform element sizes (all nav buttons the same height) allow mixing and matching. Grid-based layout
  (from print) uses a master layout as a template; most layouts use only part of it, but placement is
  always consistent. Caveat: devices and resolutions vary; adhering to a grid (or any standard) when it
  clearly no longer works is a straitjacket worse than anarchy; recognize when to revisit foundations
  (ch. 7).

### Internal and external consistency
- Internal: different parts reflect different approaches. Fix by identifying recurring elements across
  interface/navigation/information contexts, designing each once in isolation, then testing in each
  context and reworking (a big round red STOP button fine on checkout may fail on a crowded
  customization page). Objects must form a system, not just a collection of nice parts.
- External: the product differs from the organization's other products/media. Keep brand identity
  consistent at every level, from global navigation to a one-off button; inconsistency suggests a
  company "that hasn't quite figured out who it is" (ch. 7).

### Color palettes
- Brand colors (Coca-Cola red, UPS brown, Kodak yellow) consistent over years; core colors sit inside a
  broader palette chosen to complement, not compete. Brighter/bolder for foreground elements that need
  attention; muted for background. Near-identical colors in one context undermine the palette; several
  shades are fine if clearly distinguishable and used consistently (Orbitz's limited palette example)
  (ch. 7).

### Typography
- Custom typefaces (Apple, Volkswagen, London Underground, Martha Stewart) build identity; not
  required. Body text (large blocks, long reading): simpler is better (Helvetica, Times); ornate faces
  tire the eye; style needn't be sacrificed. Large text and short labels (navigation) can carry more
  personality. Too many fonts, or a few used inconsistently, create clutter; a handful suffices. Type
  rules mirror visual design: no very-similar-but-different styles; different styles only for different
  kinds of information; enough contrast to direct attention; don't overload (ch. 7).

### Design comp
- Composite visual mock-up, the surface analog of the wireframe: shows the pieces working together or
  where they break down. Expect a one-to-one correlation between wireframe and comp components; the
  layout may differ (the wireframe ignores visual concerns). Wireframing first isolates skeleton
  issues; the comp must preserve the relative importance and grouping, especially the information
  design (ch. 7).

### Style guide
- The definitive record of design decisions, largest scale to smallest: first global standards (design
  grids, color palettes, typography, logo treatment), then section/function-specific standards, down to
  individual interface and navigation elements. Why: reasons fade; people quit and take knowledge,
  giving the organization "amnesia". Goal: enough detail that future decisions are easy because the
  thinking is done. The single most effective way to make a decentralized organization's output
  cohesive; enforcement often sits high in the organization (ch. 7).

---

## 7. Applying the elements (ch. 8)

### Mindset over headcount
- Specialists bring depth; small teams can match or beat them because they stay in sync on a shared
  vision. UX design is "a very large collection of very small problems". Two ideas separate success
  from failure: understand what problem you're solving (which plane), and understand the consequences
  of your solution (the ripple) (ch. 8).

### Three unconscious design modes
- **By default:** UX mirrors the technology or organization (order history and billing in separate
  databases so kept separate in the UX; departmental content kept apart).
- **By mimicry:** copying conventions from other products regardless of fit.
- **By fiat:** personal preference (orange because an SVP likes it; dropdowns because the head engineer
  likes them) replaces objectives and user insight (ch. 8).

### "Why did you do it that way?"
- The first question to ask and be able to answer about any aspect of the experience. Adapt methods to
  time, money and people (no market research: mine server logs and feedback messages; no lab: test
  informally with friends, family, co-workers), but never gloss over fundamentals (ch. 8).

### Testing's role
- Evaluation tacked onto the end ("user acceptance testing"; "acceptance" reveals the low bar) comes
  after the chance to fix anything and after unexamined assumptions have hidden behind layers of
  interface. Testing is never a substitute for a thoughtful design process. Tests designed around the
  elements ask the right questions (navigation bar: is it the color or the wording?). Users cannot
  articulate their needs; the job is to understand them better than they do (ch. 8).

### Marathon vs sprint
- Teams in permanent emergency are behind before they start. Pace: push forward (prototypes, ideas),
  then pull back (test, see how pieces fit, refine the big picture). Deliberate decisions cost time now
  and save more later. Strategy, scope and structure are the first cuts when a project is late because
  they produce no visible component, yet they are the foundation; cutting them yields disconnected
  deliverables, a product that disappoints, and a next project spent fixing it. Upper-plane failures
  (clutter, clashing colors, poor navigation) hide lower-plane successes; upper-plane successes built
  on bad lower planes are worthless ("beautiful but utterly unusable") (ch. 8).
