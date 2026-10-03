# Examples — concrete cases from the book

Use these to cite, copy, or adapt. All from Frost (2016); stats are period snapshots.

## Ch. 1

- **30,000-page university site → 3 content types + 2 layouts.** Effort lives in
  components, not page count. Homepage: tagline+image by lunch vs carousels/forms/
  integrations over months.
- **Magic Escalator (Spool).** Big redesigns knock users down; relearning climbs
  slowly. Hence MVP + iterate over bulldoze-and-replace.
- **NPR COPE.** Create Once, Publish Everywhere — modular content to phones,
  tablets, readers, watches, TVs, consoles, signage, dashboards.
- **Style tiles (Warren) / element collages (Mall).** One-pager color/type/texture;
  exploded component collage — atmosphere without premature layout.
- **This Is Responsive.** Pattern showcase (nav, lightbox, breadcrumb, carousel
  across sizes) proving squishy pages insufficient — components have per-pattern
  challenges.
- **Bootstrap at 77k stars/30k forks.** Speed (tested, prototype, community,
  freelancer extra projects, startup MVP) vs jumpsuit sameness (childhood sci-fi:
  "we solved fashion, everyone wears jumpsuits" — humans want variety).
- **Starbucks "Blocks Three-Up" / Yelp guide home / Economist writing guide.**
  Named patterns = shared vocabulary; handsome intro (what/who/how) = invitation.
- **MailChimp (Holgado).** Library seeded from 4 primary screens → "this system
  will actually work here and here and here" — upfront cost, downstream speed.
- **"Highlight Block" without usage info.** Context failure: useful-looking pattern,
  unknown blast radius on change.

## Ch. 2

- **Water molecule (H+O → H2O; cf. H2O2).** Same atoms, different properties —
  why molecule stage earns its own level and single responsibility.
- **Search form molecule.** Label+input+button: label defines input, button submits.
  Drop anywhere search needed.
- **Header organism.** Logo + primary nav + search (+ utility nav). Heterogeneous
  section; distinct yet composed.
- **Gap product grid organism.** Same product-item molecule repeated; reusable for
  category/search/related.
- **Time Inc. homepage template → page.** Skeleton with sizes/char limits →
  Beyoncé "Moving People" reality. Skeleton guards dynamic content; page tests it.
- **Instagram native dissection.** Same five stages outside marketing web — proof
  "for UIs," with web birthplace acknowledged.

## Ch. 3 (Pattern Lab, Time Inc. + hypotheticals)

- **Block-post molecule code.** Wrapper + link + `{{> atoms-thumb }}` + h3 + p with
  `{{url/headline/excerpt}}` variables → `{{> molecules-block-post }}` reuse.
- **Header includes.** `<header>{{> atoms-logo }}{{> molecules-primary-nav }}{{> molecules-search }}</header>` → `{{> organisms-header }}` anywhere.
- **Named template instance.** `{{# factoid-advertising }}{{> organisms-factoid }}{{/ factoid-advertising }}` — wrapper name latches data override.
- **data.json → 00-homepage.json.** Lorem+FPO → Beyoncé; strings, booleans, arrays,
  conditional UI from JSON alone.
- **Collaborator dashboard + `dashboard~admin.json`.** Base list (Boomshakalaka/CIA,
  Jujubees-Daniels/long-title, Marciulionis/Warriors, Smith/Short) + `"isAdmin":true`
  → edit/delete actions. Tilde = inherit + extend.
- **ish. viewports.** Small-ish/medium-ish/large-ish randoms vs 320/480/768 device
  widths; stakeholder education bonus.
- **Code views.** Salesforce Lightning (HTML+SCSS) vs Rizzo (include-only holy grail);
  Pattern Lab template+compiled HTML, extensible to CSS/JS.
- **Annotations + lineage.** Numbered pins on living UI; `media-block` contains
  `atoms-square`+`molecules-button-bar`, used in `media-block-list` — QA scope + weed
  redundancy.

## Ch. 4

- **United.com buttons / bank buttons + forms.** Inventory screenshots exposing
  dozens of near-duplicates — the CEO-cry slide.
- **Naming collisions live.** "Utility bar" vs "admin nav" vs "floating action area"
  for one pattern — inventory as vocabulary negotiation.
- **Lego piles (Nagel).** Rummage vs organized — same bricks, deliberate/faster build.
  Hidden organizing, visible whole.
- **Three-image device story.** Desktop-only past → today's potpourri → tomorrow's
  unknown — permission to change process.
- **Waterfall theater.** Giant UX PDF signoff → comp unveiling → "fantastic, but…
  pop" pile-on → rework → dev surprise. Parallel wax-and-wane as replacement.
- **Food Bank grayscale blocks.** Crude mobile-first wireframe enough to debate
  structure/hierarchy without layout promises.
- **TechCrunch "featured island" (Brook).** Gestural site-wide display pattern, no
  aesthetic/functional assumptions — details later.
- **Spreadsheet IA.** Columns (template|display|content|order|role); left column
  read vertically = mobile-first view.
- **Gut test (Food Bank kickoff).** 20–30 sites, logo-swapped, 20s each, 1–10 vote,
  top-5/bottom-5 debate on type/color/density/illustration/vibe.

## Ch. 5

- **Dropdown global fix.** One underperforming custom dropdown → audit system →
  strip custom styling everywhere — friendly friction paying ecosystem-wide.
- **Weekend seed → official.** Hackathon library shopped around → time/money story
  + testimonials → sanctioned product (people/budget/governance/roadmap).
- **Salesforce dozen / small-org hat / consultants teach-to-fish.** Staffing by size;
  outsiders' perspective value + DNA limits.
- **Vanilla decision tree (Canonical/Persson).** Diagrammed proposal → acceptance
  path for new patterns; one-off until second "I want that!"; Sass Deprecate warnings
  + alternative before removal.
- **Rizzo/Twig/Drupal/Starter 8 bridges.** Steps toward holy grail (one edit →
  library + production).
- **Carousel as cross-discipline stress test (Walmart).** Business/editorial/copy/art/
  UX/frontend/backend converge — one pattern page must house all concerns.
- **Yelp home / Material changelog / Harmony hub / U.S. Web Standards GitHub issues /
  Shyp PR→Slack.** Approachable entry, visible change, bigger co-housing, maintained
  conversation — plus public Bat-Signal hiring (Bolton → Salesforce).
- **Blur-to-name + "carousel"/"card".** Content-blurred naming for structure truth;
  Material photos/videos + lineage for usage truth.
