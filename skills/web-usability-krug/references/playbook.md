# Playbook — task-oriented procedures from Don't Make Me Think, Revisited

Each section: when you are doing X, these are the steps, checks and decision rules, with chapter sources. The full usability-test procedure lives in `usability-test-kit.md`; page audit checklists in `trunk-test.md`.

## Contents
1. Reviewing a page or screen (expert usability review)
2. Designing or fixing navigation
3. Designing or fixing a Home page / landing page
4. Writing and cutting copy, labels, instructions, FAQs
5. Designing a choice, question or form step
6. Deciding convention vs. innovation (and flat design)
7. Settling a design argument
8. Reviewing a mobile site or app
9. Courtesy / goodwill audit
10. Accessibility quick start
11. Getting management to care; building a practice
12. Handling requests to manipulate users

---

## 1. Reviewing a page or screen (expert usability review) (Intro, ch. 1–5)

Krug's own first step is to try to use the thing as its users would and note where people are likely to get stuck or confused. Do this before any checklist.

1. **Pick 2–3 real tasks** a typical user would come to do (ch. 11: ask "what are the three main things users want to do here?").
2. **Do the neighbor test** (ch. 1): could someone with no interest in the subject, who barely knows the Back button, glance at this and say "Oh, it's a ____"? If not, the big picture is missing — go to §3.
3. **Squint / arm's length pass** (ch. 3, 6). Without reading details, can you point at the areas and name them ("navigation", "things I can do", "stuff they're selling me")? Is there a visual hierarchy (importance → prominence; related → grouped; nested → spanned)? Does anything shout? Is it on a grid? Is it cluttered? If this is an interior page, run the trunk test (`trunk-test.md`).
4. **Hunt question marks** (ch. 1). For each element ask: Where am I? Where should I begin? Where did they put ___? What's most important here? Why did they call it that? Is that an ad or content? Is this clickable? Record each as a finding with its cause category:
   - name problem (cute, marketing, company-specific, technical)
   - clickability ambiguity (same color as headings; no shape/location cue; hover-only cue on touch)
   - hard choice (user can't tell which option is "me"; options presented all at once)
   - scent problem (link wording doesn't unambiguously identify the target)
   - noise (shouting, disorganization, clutter)
   - wall of words / happy talk / instructions
   - missing navigation element (see §2)
   - goodwill drain (see §9)
5. **Count the words** (ch. 5). Can half be removed? Welcome text, intros on section fronts, instructions: cut or delete.
6. **Check scannability of text** (ch. 3): headings (enough? distinct levels? not floating?), paragraph length, lists, bold key terms.
7. **Prescribe fixes**, cheapest first (ch. 9): prefer removing what obscures over adding explanations; prefer the convention; make cues twice as prominent as feels tasteful; if a difficult choice remains, add guidance that is brief, timely, unavoidable (ch. 4).
8. **Rank** findings by seriousness (what would stop most users from completing the main tasks), not by ease of fixing; note which are "kayak" problems to ignore (ch. 9).
9. **Recommend observation**: for anything you're guessing about ("will users understand this label?"), say so and propose a 3-user test (§7, `usability-test-kit.md`).

## 2. Designing or fixing navigation (ch. 6)

**Decision rules**
- Persistent navigation on every page: Site ID, Sections, Utilities, Search, Home. Exception: form pages (checkout, registration, subscription, feedback, preferences) — reduce to Site ID + Home + utilities that help complete the form.
- Site ID: top of page, usually upper-left; looks like a logo (distinctive typeface, graphic recognizable from button to billboard); links Home. Include "Home" among the sections too.
- Sections = top level of the hierarchy. Decide where secondary navigation lives: in the persistent nav, in a dropdown (hover/click), or on the section front. Whatever you choose, show it on sample pages for *every* level.
- Utilities: at most 4–5 in the persistent nav (Sign in/Register, Help, Cart, About, Contact...); the rest in the footer. Slightly less prominent than Sections.
- Search: a box (not a link), a button, the word "Search" or the magnifying glass. Button label "Go" if the box is labeled "Search." No "Find/Quick Search," no "type a keyword," no scope or field options up front; show scope only if confusion is possible (site vs. whole Web); put scope narrowing on the results page.
- Page name on every page, framing the unique content, usually the largest text, matching the clicked link's words (or as close as possible with an obvious reason).
- "You are here" in every nav structure on the page (section and subsection), with at least two distinctions (color + bold).
- Breadcrumbs when the site is large and deep: top of page, `Home > Section > Subsection > **Current page**` (last item bold, unlinked).
- Tabs if you want a self-evident, hard-to-miss primary nav: active tab in a contrasting color, physically joined to the content panel.
- Visited links visibly different from unvisited (ch. 13).

**Procedure for a navigation design**
1. Write down the hierarchy to its deepest level with real sample content for lower pages (demand it from content owners; they usually haven't thought that far).
2. Produce sample pages for Home, a section front, a second-level page, and the deepest level — before debating colors.
3. On each, mark the six trunk-test elements. Squint: do they pop?
4. Walk the chainsaw scenario: a user wanting X — which section sign do they pick? Is that choice mindless (ch. 4)? If two sections plausibly contain X, either cross-list or rename.
5. Check the social contract: every link text vs. destination page name.
6. Check lower-level consistency: does level 3 use the same nav scheme as level 2, or has it become ad hoc?
7. Simulate arrival from search/social on a deep page: can the diver "bob up" to Home and understand the site?

## 3. Designing or fixing a Home page / landing page (ch. 7)

1. **Inventory obligations**: identity & mission; hierarchy (persistent nav); search; teases (content promos, feature promos); timely content / signs of life; deals; shortcuts; registration/sign-in state. Plus the abstract goals: what I'm looking for, what I'm not looking for, where to start, credibility.
2. **Protect the big picture first.** Draft explicit answers to the four questions — what is this, what can I do here, what do they have here, why here and not elsewhere — then decide where each is answered: tagline (next to Site ID), Welcome blurb (prominent block, top-left or center), "Learn more" (short video for novel propositions).
3. **Write the tagline**: 6–8 words; clear and informative; differentiating ("no one else could use it"); benefit-bearing; lively; not a motto, not generic, not a mission statement. Even household names should have one — the online mission differs from offline.
4. **Size the explanation**: as much space as needed (Kickstarter devotes most of Home to explaining itself) but no more (full-page manifestos don't get read; a few key features).
5. **Answer the fifth question**: make entry points look like entry points and label them — "Search," "Browse by Category," "Sign in," "Start here" for step-by-step processes. Make the primary process's entry leap out (mortgage application). Check that promos don't drown them.
6. **Run the commons check**: list every promo; for each, who gains (+1) and who pays (everyone). Propose rotation or cross-promotion from other popular pages for the losers. Remember it degrades one item at a time.
7. **Test it with outsiders**: show the Home page to people outside the organization and ask what it is — the Home page tour step of a test session (`usability-test-kit.md`). Insiders will never notice the main point is missing.
8. **Every deep page orients too**: Site ID + tagline, page name, sections — because most visitors never see Home first.

## 4. Writing and cutting copy, labels, instructions, FAQs (ch. 1, 3, 5, 11)

**Cutting**
1. Apply the Third Law literally: target half the words, then look for half of what's left.
2. Delete happy talk: any text that passes the "blah blah blah" test — welcomes, "how great we are," section-front intros that merely describe the links below.
3. Delete instructions where the interface can be made self-explanatory; where unavoidable, cut to the minimum (103 → 34 words in the survey example: purpose + time needed + the one exception that matters).
4. Replace mission-statement prose with what you actually do.

**Formatting for scanning** (ch. 3)
- Headings: more than you think; each an honest label or an intriguing hook; levels visibly distinct (size or space above); never floating — tighter to the text below than above.
- Paragraphs: short; one sentence is fine; split long ones at the natural break.
- Lists: any comma/semicolon series becomes bullets; small extra space between items.
- Bold key terms at first appearance, sparingly; not when they're already links.

**Naming** (ch. 1, 6)
- Prefer the obvious word over cute, branded, internal or technical names ("Jobs," not "Job-o-Rama"). Push the tradeoff further toward obvious than the team wants.
- Link text must give strong scent: it names its destination unambiguously; the destination's page name repeats those words.
- Search is "Search." Entry points are "Search," "Browse by Category," "Sign in," "Start here."

**FAQs and support content** (ch. 11)
- Only real frequently asked questions — not QWWPWAs ("Questions We Wish People Would Ask").
- Get this week's top five from Customer Service/Support and put them at the top of the Support page; keep it current.
- Be candid about what people would rather not hear (shipping costs, outages, fees, strikes).
- If you can't do what they want, say you know it's an inconvenience.

**Accessibility of text** (ch. 12): put the keyword at the *start* of links and lines — screen-reader users hear the first few words and move on.

## 5. Designing a choice, question or form step (ch. 4, 11, 13)

1. **Make each choice mindless.** Test: could a user answer it as easily as "animal, vegetable, or mineral?" If the user has to classify *themselves* (home office vs. small business; subscriber vs. member) and could be wrong, redesign: ask one simple question, then show only the relevant follow-up on the next screen (NYTimes pattern).
2. **Prefer more mindless clicks over fewer thoughtful ones** (three mindless clicks ≈ one thoughtful click), except on paths users repeat constantly or where pages load slowly.
3. **Give guidance only where needed**, and make it brief, timely, unavoidable: inline tips next to the field, "What's this?" links, tooltips (not on touch — no hover). Never a paragraph of instructions above the form.
4. **Don't punish formatting**: accept dashes/spaces/parentheses in SSNs, card numbers, phone numbers; normalize in code.
5. **Ask only for what the task needs**; a long registration form can empty the goodwill reservoir in one step.
6. **Labels outside fields** unless all five conditions in ch. 13 hold (very simple form; label disappears on typing and returns when emptied; can't be confused with an answer; can't be submitted with the input; fully accessible). Use `<label>` elements (ch. 12).
7. **Error recovery**: where errors are unavoidable, provide a graceful, obvious way back; test to eliminate the avoidable ones.
8. **Strip persistent navigation** on form pages to Site ID, Home and helpful utilities so nothing competes with finishing.
9. **Let test participants pick details** when testing forms ("find a book you want to buy") to raise emotional investment.

## 6. Deciding convention vs. innovation (and flat design) (ch. 3, 10)

Decision tree:
1. Is there an existing convention for this element (location, behavior, look, genre pattern)? If yes and you have no clearly better idea → use it.
2. If you want to replace it, the replacement must satisfy one of: (a) so clear and self-explanatory that there's no learning curve; or (b) adds so much value that a small learning curve is worth it. If neither can be shown → convention.
3. If you innovate (Harlem.org photo navigation), also provide the conventional path alongside it.
4. Consistency argument on the table? Ask: would the inconsistency make this *significantly* clearer? If yes, clarity wins.
5. Flat/minimal styling requested? List the affordance dimensions you're removing (bevel, border, shadow, underline, color). For each clickable/typeable element, ensure at least two remaining dimensions still signal it (position + reversed type/all caps; border on inputs; color + shape on buttons). Nothing may depend on hover.
6. Custom replacements for OS/browser widgets (scrollbars, selects, date pickers): assume you're discarding hundreds of hours of tuning; justify under rule 2 or don't.
7. Awards, novelty and peer praise are not reasons (ch. 3).

## 7. Settling a design argument (ch. 8)

When the team is debating "which is better" or "what users like":
1. Name it: this is a religious debate (personal taste + professional lens + hype-vs-craft), and it has no winnable answer because there is no Average User.
2. Reframe the question from the general ("do people like carousels?") to the specific: "Does *this* carousel, with these items and this wording, in this context, on this page, create a good experience for most people likely to use this site?"
3. Pick the cheapest testable version — sketch, wireframe, or crude prototype. Build it.
4. Run 3 participants on 2–4 tasks (`usability-test-kit.md`). Observe; don't ask opinions.
5. Decide on "works / doesn't work," not on preferences. Expect that the test will often show the argued-about element didn't matter and something upstream (the value proposition, the page name) is the real problem — "windows, not drapes."
6. If someone insists on aesthetics feedback: ignore color comments unless three of four participants say "puke" (ch. 11).

## 8. Reviewing a mobile site or app (ch. 10)

**Tradeoff audit**
1. For each annoying behavior, identify the constraint behind it (ad page views, CMS segmentation, performance budget) and ask whether the tradeoff weighed user experience enough. State the user cost in concrete terms (CBS: tap, wait, scroll past photo, read two paragraphs, repeat 8 times).
2. Prioritization: list what users do in a hurry or frequently → one tap away; everything else reachable by an obvious path within a few taps. Don't cut features on the "on the move" assumption; people use phones on the couch and expect everything.
3. Depth: 3–5 levels is acceptable if scent holds at every tap (clear labels, confidence the target is behind the link).

**Mobile web checklist**
- Zooming allowed (no `user-scalable` lock or tiny fixed text).
- Deep links from email/social land on the content, not the mobile Home.
- Mobile Site / Full Site toggle at the bottom of every page.
- Responsive build doesn't ship oversized images/code; test on 3G/4G, not only Wi-Fi.
- Nothing requires hover: no hover-only tooltips, hover-only menus, hover-revealed clickability.

**Affordance checklist**
- Every tappable element has visible cues (shape, border, color, position); every input has a visible boundary.
- If the design is flat, each interactive element still carries ≥2 distinguishing dimensions.
- Affordances needed for the main tasks are noticeable without hunting.

**App learnability / memorability**
- If the app has more than a few features or unconventional gestures: provide a findable tour/help (not just two launch screens you can't reopen); make the structure (levels: lists / items / settings) visible so users can navigate between levels; make Help reachable from a stuck state (avoid the Catch-22).
- Test the primary task on first use after the tutorial ("create a list called Chicago trip with three items"); if participants fail, learnability is the serious problem regardless of reviews.
- Memorability: prefer visible controls over hidden gesture-only controls (ASketch); if controls are hidden for canvas space, make the reveal gesture a convention, not a trick.
- Delight is extra credit; verify the core is learnable, effective and efficient first.
- Speed: show the thing the user tapped for before loading everything else (AP alert anti-pattern).

**Mobile testing**: same script as desktop; solve logistics with a device-mounted camera (see `usability-test-kit.md` §9).

## 9. Courtesy / goodwill audit (ch. 11)

1. **Name the three main things** users come to do. Verify each is obvious and easy and nothing gets in the way (nothing should get in the way of applying for a mortgage on a mortgage site).
2. **Walk the reservoir**: as a slightly annoyed, hurried user, step through a key task and log each goodwill hit (−) and refill (+). Remember reserves are idiosyncratic and situational — assume a small one.
3. **Diminishers to find and remove**
   - Hidden support phone numbers, shipping rates, prices, fees (show the 800 number in plain sight, even on every page; show cost before the third screen).
   - Format punishment (spaces, dashes, parentheses rejected).
   - Unnecessary personal data requests.
   - Faux sincerity ("your call is important to us").
   - Sizzle in the way (marketing photo pages before content).
   - Amateurish, sloppy appearance.
   - Silence on the one thing everyone is asking (strike day: "What's going to happen to me?").
4. **Refills to add**
   - Upfront candor on shipping, parking fees, outages.
   - Steps saved (tracking link that submits the number).
   - Effort visible in support content (HP model: generate, verify, present, organize).
   - Real, current, candid FAQs (support's top five this week at the top).
   - Printer-friendly pages (drop ads, keep figures).
   - Graceful error recovery.
   - Apologies where you can't do what they want.
5. **Deliberate unfriendliness** (pop-ups, upsells): acceptable only as an informed business decision with the user cost acknowledged.
6. **Appearance comments** from users: log but don't act on color opinions unless three of four say "puke."

## 10. Accessibility quick start (ch. 12)

Order matters:
1. **First, fix what confuses everyone** — run usability tests and smooth the confusing parts; this is the single best accessibility improvement and a prerequisite for everything else.
2. **Three-second test**: raise the browser text size; if nothing changes, fonts are fixed-size — fix that.
3. **Learn how screen-reader users work** (Theofanos & Redish, 20 minutes): they scan with their ears; front-load keywords in links, headings and lines; many run speech very fast.
4. **Low-hanging fruit**
   - `alt` on every image: `alt=""` for decorative, descriptive text otherwise (webaim.org for how).
   - Semantic headings in order: h1 page title, h2 sections, h3 subsections; style via CSS.
   - `<label>` bound to every form field.
   - "Skip to Main Content" link first on every page.
   - Full keyboard operability.
   - Strong text/background contrast; never light grey on dark grey; never small low-contrast type (ch. 13).
   - Accessible template/theme if using a CMS.
5. **Validators**: use them for the clear errors (missing alt); don't let the vague warnings discourage or define the work.
6. **Buttered cats**: when a request pits accessibility against mainstream design, look for the Plexiglas-overlay solution that gives each audience the best experience rather than halving both.
7. Then read Horton & Quesenbery or Thatcher et al. for the big picture.

## 11. Getting management to care; building a practice (ch. 9, 13)

1. **Get the boss (and the boss's boss) into a live test session.** Frame it as "poke your head in for a few minutes — good for team morale." Expect them to stay. Fallback: <3-minute highlight clip on the intranet with an intriguing email; clips in presentations.
2. **Do the first test on your own time**: no permission, volunteers as participants, incredibly simple. Choose a target with one serious problem you can fix without sign-offs (a badly labeled button). Test → fix → publicize. Measure if cheap (support calls on that issue before/after).
3. **Test the competition** as a brown-bag event: everyone loves it, no one is defensive, and it doubles as pre-design research (ch. 9).
4. **Institutionalize cadence**: one morning a month (3 users, debrief at lunch), fixed day (e.g., third Thursday); Agile: 2 users every two weeks. Never tie testing to milestones.
5. **Grow observers**: snacks (chocolate croissants, good pizza), predictable schedule, observation room with big screen and speakers.
6. **Speak business where you can** (ROI, pain points, KPIs) but don't depend on it; ROI cases are laborious and contestable.
7. **Empathize with management** and stay humble: share what you know; don't preach.
8. When others claim "it's all UX now," ask how they learn about users, how they test, and how they get changes made.
9. Further reading: Sharon, *It's Our Research*; Buley, *The User Experience Team of One* (ch. 3–4); Bias & Mayhew, *Cost-Justifying Usability*.

## 12. Handling requests to manipulate users (ch. 13)

- Influence and persuasion are legitimate (Cialdini; Weinschenk) as long as they are not deceptive; think-aloud testing can reveal why persuasion works or fails.
- Usability testing cannot measure desirability — only market research can. Decline "run a usability test to prove people want this."
- Refuse dark patterns: pre-checked hidden opt-ins, decoy "Start Download" buttons, silent toolbar/search/Home-page changes, anything shading into phishing or scams. "If people ask you to do any of this, it's not part of your job. The users are counting on you."
- Offer the honest alternative: make the thing genuinely clearer and more desirable, and show candor (ch. 11) — it refills goodwill rather than draining it.
