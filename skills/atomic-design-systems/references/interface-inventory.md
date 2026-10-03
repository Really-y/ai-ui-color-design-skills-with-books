# Interface inventory — runnable procedure (Frost, *Atomic Design*, ch. 4; naming tips from ch. 5)

An interface inventory is "a comprehensive collection of the bits and pieces that make up your user
interface": screenshots of **one instance of each unique UI pattern**, loosely categorized. It is the
UI counterpart of a content inventory. Frost uses it to (a) make stakeholders "feel the pain" of an
inconsistent UI, (b) establish a shared vocabulary, (c) scope the work, and (d) seed the pattern
library. Example output: every unique button style on United.com's homepage; "37 unique button styles"
on a major bank's site.

## Contents

1. When to run it
2. Pre-flight checklist
3. Step 1 — Round up the troops
4. Step 2 — Prepare for screenshotting
5. Step 3 — Screenshot exercise (categories, timing, coverage)
6. Step 4 — Present findings
7. Step 5 — Regroup and establish next steps
8. Templates (invite, slide deck structure, capture log, consolidation sheet, decision sheet)
9. Benefits to cite when pitching
10. Running it solo or with an AI assistant (extractor note)

---

## 1. When to run it

- Before pitching a design system, when words have not convinced stakeholders ("Sometimes you need to
  make them feel the pain").
- At the start of a redesign, replatform or any project you can piggyback a pattern library onto.
- When naming patterns: the inventory "helps remove patterns from the context of the page where they
  normally reside" so names are not distracted by context (ch. 5).
- Again, later, with a smaller group, to fill gaps ("It's very likely the initial exercise didn't
  capture every unique UI pattern").

## 2. Pre-flight checklist

- [ ] A leader who will combine everything into the "über-document".
- [ ] One shared capture tool agreed by everyone (see Step 2).
- [ ] A list of all properties/surfaces to cover: main site, app, support, FAQs, sizing charts, 404s,
      legal/terms, email templates, third-party-hosted experiences (payment portals, localized sites).
- [ ] Access to logged-in, admin, error and empty states (messaging often "requires user action to
      expose").
- [ ] Screen-recording software for the Animation category (QuickTime or equivalent).
- [ ] Optional style-guide bootstrapping tools for Colors: CSS Stats, Stylify Me.
- [ ] Timer and upbeat music; snacks for the break.

## 3. Step 1 — Round up the troops

"It's absolutely essential to get all members of the team to experience the pain of an inconsistent UI
for them to start thinking systematically." Invite representatives from **all** disciplines
responsible for the site: UX designers, visual designers, front-end developers, back-end developers,
copywriters, content strategists, project managers, business owners, QA, other stakeholders. "The more
the merrier" — one of the most crucial results is a shared vocabulary, which needs everyone's input.
(A lone ambitious designer documenting patterns is applauded but insufficient.)

## 4. Step 2 — Prepare for screenshotting

Possible tools: PowerPoint or Keynote; Photoshop or Sketch; Evernote Web Clipper; Google Docs or
Word; Google Slides (Frost provides a Google Slides interface inventory template). The tool does not
matter, but **everyone must use the same one** so the results can be combined. Frost prefers online
slides: a free-form canvas for images, slides as natural category chunks, web-based sharing.

## 5. Step 3 — Screenshot exercise

Rules:
- Capture **one instance of each unique pattern**, not every instance.
- Assign each participant one UI category (pair people or give multiples depending on headcount).
- **Time-box: 30-90 minutes** for a first pass. Set a timer. Don't let it eat the whole day.
- **Dig deep: capture everything** that "is or could be managed by your organization". Organizations
  favour the homepage and the core flow; also cover customer support, FAQs, sizing charts, 404 pages,
  legal terms. "Users perceive your brand as a singular entity and don't care about your organizational
  structure, tech stack, or anything else."

Starting categories (add, subtract or modify to fit your UI):

| Category | What to capture |
|---|---|
| Global elements | headers, footers, anything shared across the whole experience |
| Navigation | primary nav, footer nav, pagination, breadcrumbs, interactive component controls — anything used to move around the UI |
| Image types | logos, hero images, avatars, thumbnails, backgrounds, any other image pattern |
| Icons | magnifying glasses, social icons, arrows, hamburgers, spinners, favicons, every interface icon |
| Forms | inputs, text areas, select menus, checkboxes, switches, radio buttons, sliders, other inputs |
| Buttons | every unique button: primary, secondary, big, small, disabled, active, loading, buttons that look like text links |
| Headings | h1-h6 and typographic variations |
| Blocks | touts, callouts, summaries, ads, hero units — combinations of heading and/or image and/or summary text (Nicole Sullivan's media object) |
| Lists | unordered, ordered, definition, bulleted, numbered, lined, striped, any list-type grouping |
| Interactive components | accordions, tabs, carousels, other modules with moving parts |
| Media | video players, audio players, rich media |
| Third-party components | widgets, iframes, stock tickers, social buttons, invisible tracking scripts — anything not hosted on your domain |
| Advertising | all ad formats and dimensions |
| Messaging | alerts, success, errors, warnings, validation, loaders, popups, tooltips (hard to capture; needs user action) |
| Colors | every unique colour (CSS Stats, Stylify Me help) |
| Animation | screen-record anything that moves, fades, shakes, transitions |

## 6. Step 4 — Present findings

1. Take a break first (food, coffee, stretch) — the exercise is overwhelming.
2. Each participant presents their category for **5-10 minutes**.
3. Discuss the rationale behind existing patterns; kick-start the naming conversation ("Oh, we call
   that the utility bar." / "the admin nav" / "the floating action area!"); name previously unlabeled
   patterns. Do **not** force consensus on final names in ten minutes — this opens a broader discussion.
4. Everyone sends their slides to the leader, who combines them into one über-document — "a wrecking
   ball of truth and justice".

## 7. Step 5 — Regroup and establish next steps

- Show the über-document to anyone, including non-designers and executives: inconsistency is
  self-evident ("Have you ever wanted to see a CEO cry?").
- Run a second, gap-filling audit if needed; then a **smaller cross-disciplinary working group** goes
  through the document and answers:
  1. Which patterns should stay, which should go, and which can be merged together?
  2. What pattern names should we settle on? (Use the ch. 5 rules: name by structure, not by page
     location or content — "carousel" not "homepage carousel", "card" not "product card"; blur the
     content in screenshots so names reflect structure.)
  3. What are the next steps to translate the inventory into a living pattern library?
- Translate the discussion into the seeds of the design system and pattern library.

## 8. Templates

### 8a. Invitation (fill in)

```
Subject: Interface inventory workshop — [date], [60-90 min + 60 min debrief]

We're going to screenshot and categorize every unique UI pattern across [product(s)] so we can
see our interface as a whole and agree on what we call things. We need every discipline in the
room: [UX, visual, front-end, back-end, content, copy, PM, business owner, QA].

Bring: a laptop with access to [surfaces incl. logged-in/admin/error states], [Google Slides]
(we all use the same tool so slides can be merged), screen recording for animation.
Your category: [see assignment list]. Time-box: [45] minutes of capture, then a break, then each
person presents for 5-10 minutes.
```

### 8b. Slide-deck structure (one deck per participant, same template)

```
Slide 1  Category: <name>   Owner: <person>   Surfaces covered: <list>
Slide 2+ One slide per *unique* pattern:
         - screenshot (cropped to the pattern; optionally a second with content blurred)
         - where found (URL / screen)   - current name(s) people use
         - states seen (hover / active / disabled / loading / empty / error)
         - notes (why it differs from similar ones; suspected duplicate of ...)
Last     Open questions for the debrief
```

### 8c. Capture log (optional spreadsheet; one row per unique pattern)

| # | Category | Screenshot ref | Found at (URL/screen) | Names in use | States captured | Looks like (possible duplicate) | Owner |
|---|---|---|---|---|---|---|---|

### 8d. Consolidation sheet (leader, after merge)

| Category | Unique patterns found | Obvious duplicates | Missing states/edge cases | Surfaces not yet covered |
|---|---|---|---|---|

Headline numbers to pull out for stakeholders: "N unique button styles", "N distinct heading
treatments", "N colours of grey", "N carousels".

### 8e. Decision sheet (working group, Step 5)

| Pattern (working name) | Decision: keep / merge into ... / retire | Agreed name (structure-based) | Stage guess (atom / molecule / organism) | Content it must hold (image sizes, char lengths) | Owner | Next step |
|---|---|---|---|---|---|---|

Check each agreed name against ch. 5: does it describe where it lives (bad) or what is inside it
(bad) rather than its structure (good)?

## 9. Benefits to cite when pitching (ch. 4)

1. **Captures all patterns and their inconsistencies** — similar-but-different patterns side by side
   expose redundancy.
2. **Gets organizational buy-in** — a diverse group experiences the problem; the über-document
   convinces bosses and clients to invest.
3. **Establishes a scope of work** — effort per pattern; which components are easy or hard to make
   responsive; content, design and development considerations per component; realistic scope and
   timeline.
4. **Lays the groundwork for the design system** — decides which patterns make the final cut and
   establishes the shared vocabulary.

## 10. Running it solo or with an AI assistant (extractor note)

Frost insists on the group format because buy-in and vocabulary come from shared pain. If you must
start alone (or an assistant is asked to inventory a codebase or screenshots), keep Frost's rules —
one instance per unique pattern, the category list above, everything managed by the organization,
structure-based names — and treat the result as the "make a thing" step of ch. 5: a tangible draft to
shop around, followed by the real group session.
