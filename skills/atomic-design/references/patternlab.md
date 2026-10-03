# Pattern Lab mechanics — from includes to lineage

Source: *Atomic Design* ch. 3 (pp. 64–92). Principles transfer to any tool; Pattern
Lab (Olsen, Muenzenmeyer, Frost — PHP or Node engine) is the worked example.

## What Pattern Lab is / isn't

- Is: static-site generator (source patterns → compiled frontend UI in library
  shell) + pattern documentation/annotation tool + starter kit.
- Isn't: UI framework (Bootstrap/Foundation), language/library/style-dependent,
  CMS replacement.
- Deliberately ugly default dashboard: so nobody mistakes demo UI for suggested
  styles. You own look/feel, naming, syntax, libraries. Can even use Bootstrap
  inside it — it just stitches.
- Backend-agnostic output (HTML/CSS/JS). Don't need PHP/Node mastery ("don't need
  to build an engine to drive a car") — choose what fits org infra and team habits.

## Nesting dolls + includes (DRY)

- Model: Matryoshka dolls — atoms inside molecules inside organisms inside
  templates. Change once → everywhere employing it updates. Beats sifting hundreds
  of PSDs for every instance.
- Mechanism: Mustache includes. `{{> atom-thumbnail }}` finds atom "thumbnail".
  Folders renamable (atoms/molecules/organisms/templates/pages labels changeable) —
  team-effective categorization beats canonical purity.
- Worked chain (Time Inc.):
  - `molecules-block-post`: `<div class="block-post"><a href="{{url}}">{{> atoms-thumb }}<h3>{{headline}}</h3><p>{{excerpt}}</p></a></div>`
  - include as `{{> molecules-block-post }}`
  - `organisms-header`: `<header>{{> atoms-logo }}{{> molecules-primary-nav }}{{> molecules-search }}</header>` → `{{> organisms-header }}`
  - homepage template pulls header/footer + named sections:
    `{{> organisms-header }}<main>{{# hero }}{{> molecules-hero }}{{/ hero }}<section>{{# experience-block }}{{> molecules-block-main }}{{/ experience-block }}...` — small patterns already built, template only places + names instances (`factoid-advertising` wrapper lets content latch on).

## Data: defaults → page overrides (structure ≠ content)

- Side-by-side: left template (content structure: grayscale, dimensioned images,
  char limits), right page (real content). Template proves skeleton; page proves reality.
- `source/data.json` defaults: `"hero": {"headline":"Lorem Ipsum","img":{"src":"/images/sample/fpo_hero.png","alt":"Hero Image"}}`
- Per-page override `pages/00-homepage.json`: same keys → `"Moving People"` +
  `"/images/hero_beyonce.jpg"`. Extends to booleans, arrays/loops, dramatic UI
  switches via JSON alone.
- Four payoffs: (1) DRY split — change structure without touching every data
  instance and vice versa; (2) ad hoc CMS without WordPress/Drupal/MySQL;
  (3) backend blueprint — backend devs see static vs dynamic bits to wire to real
  CMS; (4) non-devs (writers/content) edit safely, freeing frontend from
  death-by-typo-cuts.

## Pseudo-patterns for variations (design the worst case)

- Problem: static tools design only best cases (Sara Smith fits one line, magazine
  avatar, full profile, equal columns). Reality: no avatar? 87 cart items? 14 product
  options? 400-char title? first-time vs returning? zero vs 7-nested comments?
  urgent dashboard message?
- Fix: `pages/dashboard~admin.json` — tilde = pseudo-pattern inheriting
  `dashboard.json` + override/append. Set `"isAdmin": true` → conditionally render
  edit/delete actions on collaborator blocks (Steve Boomshakalaka/CIA, long company
  name, Marciulionis/Warriors, Sara Smith/Short Title test overflow).
- Rule: every pattern ships with its "what-if" set. Static-tool tedium is no excuse
  in a data-driven library.

## Viewport fluidity (ish.)

- Goal: resilient versatile components placeable full-bleed, in-article, or sidebar —
  container-query mindset before native support (media queries = viewport; container
  queries = parent).
- Anti-tool: 320/480/768 device-width testers (iPhone4 portrait/landscape, iPad).
  Web is a spectrum, not 3 views.
- ish.: small → small-ish viewport (re-click → different small-ish), medium →
  medium-ish, large → large-ish. Randomized values force spectrum thinking + bug
  discovery. Baked into Pattern Lab. Bigger win as education: stakeholders see
  system must work at any width.

## Code view (right code, not all code)

- Baseline: HTML for every pattern (copy-paste speed + syntax/style enforcement
  across many devs). Add pattern CSS/JS per org (Salesforce Lightning: HTML+(S)CSS).
- Holy-grail variant: expose only include (Lonely Planet Rizzo: `{{> pattern }}`),
  single source of truth maintained by core team — devs pull, never fork code.
- Pattern Lab shows template code + compiled HTML; extendable to CSS/JS.
- Rule: showcase code that makes your team effective, not maximal code.

## Living docs + annotations (never PDFs)

- Old way: giant wireframe/spec PDFs debated, approved, then trashed at production.
- New: per-pattern Markdown (`pattern-name.md`) in list view (definitions, usage,
  examples, resources) + interactive annotations pinned to living UI (numbered
  elements → click jumps to note). Covers a11y, performance, aesthetics in context.
- Payoff: insights from every discipline live where the UI lives.

## Lineage (paper trail for change)

- Answers "great, but where is this used?" Auto-generated from includes.
- Example: `media-block` molecule (image+headline+text+button-bar) contains
  `atoms-square` + `molecules-button-bar`; used in `media-block-list` organism.
- Uses: scope QA/retest on change (double image? add element? → know every
  template to retest); spot redundant/underused patterns to weed pre-launch.

## Six-quality vetting checklist (any tool)

1. Descriptions + annotations.
2. Relevant code (HTML/template/CSS/JS as needed).
3. Full-spectrum viewport viewing.
4. Variations (active/disabled, admin/user, empty/full).
5. Dynamic real representative content in structures.
6. Lineage/context (contains + where-used).
- Closing line of chapter: not about tools, but how you use them to change
  culture/process/workflow (bridge to ch. 4–5).
