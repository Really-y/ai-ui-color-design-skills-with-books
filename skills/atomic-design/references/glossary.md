# Glossary — Atomic Design terms as Frost uses them

- **Atom:** smallest functional UI unit (label, input, button, heading, image).
  Indivisible without losing function + intrinsic properties. Library base-styles reference.
- **Molecule:** simple group of atoms with one job (search form). Single-responsibility,
  testable, portable.
- **Organism:** distinct interface section (header; product grid). Heterogeneous (dissimilar
  parts) or homogeneous (repeated molecule). Provides context.
- **Template:** page-level layout + content structure (sizes, lengths), not final content.
  Skeleton proving parts compose.
- **Page:** template + real representative content. Most concrete; user truth + signoff truth.
- **Mental model (not linear process):** five stages concurrent; explanation order ≠ execution order.
- **Part and whole:** traverse abstract↔concrete (painter stepping back/in). Fix small,
  judge big.
- **Content vs display pattern:** content = what (article, product); display = gestural
  container ("featured island") usable anywhere. Spreadsheet articulates both + order + role.
- **Design atmosphere:** feel/mood/identity independent of layout (Clarke). Explored via
  tiles/collages, not comps.
- **Style tile (Warren) / element collage (Mall):** lo-fi atmosphere explorations (color/type/
  texture; exploded components).
- **Interface inventory (audit):** systematic screenshot capture → categorize → present →
  über-document → keep/merge/drop + scope. Both diagnostic and sales tool.
- **Über-document:** merged inventory deck laying bare inconsistencies (CEO-cry artifact).
- **COPE:** Create Once, Publish Everywhere (NPR). Structured chunks → any platform.
- **Magic Escalator (Spool):** acquired-knowledge climb users lose in big redesigns.
- **Pattern library / style guide:** living hub of components + docs (vocabulary, education,
  testing, speed, longevity). Frost uses interchangeably; "guide" often = library + docs shell.
- **Pattern Lab:** static-site generator + docs/annotation + starter (Olsen/Muenzenmeyer/Frost).
  Not framework/CMS. PHP or Node engine; backend-agnostic output.
- **Include:** `{{> atoms-thumb }}` — nesting-doll composition; DRY single source.
- **Mustache section:** `{{# name }}...{{/ name }}` — named template instance latchable by data.
- **data.json → page JSON:** defaults → per-page overrides (strings, booleans, arrays, flags).
- **Pseudo-pattern (`~`):** `dashboard~admin.json` inheriting base + overrides (e.g. `isAdmin`).
  Variation without duplication.
- **ish.:** randomized small/medium/large-ish viewport tester; spectrum > devices.
- **Container-query mindset:** components adapt to parent container, not viewport (native
  support pending in 2016; principle stands).
- **Code view:** exposed HTML/template/CSS/JS per team need; Rizzo include-only at grail.
- **Annotation:** numbered note pinned to living UI (a11y/perf/rationale in context).
- **Lineage:** auto contains + where-used trail (what composes it; where employed). QA scope + weed tool.
- **Holy grail:** library ↔ production sync; one edit updates both. Bridges: Rizzo/Twig/Drupal/Starter 8.
- **Makers vs users (Bolton):** makers govern/create (birds-eye); users apply/report (on-ground).
  "System informs product, product informs system."
- **Friendly friction:** system-first checkpoint forcing ecosystem consideration over page hotfix.
- **Governance:** nine-Q plan (modify/swap/create, requests, retirement, bugs, approver, docs,
  coder, deploy, announce) + rituals (office hours, state-of-union).
- **Three pattern changes:** modify (refresh), add (one-off until second use + decision tree),
  remove (Sass-Deprecate warning + alternative, never rug-pull).
- **Ten makes:** official, adaptable, maintainable, cross-disciplinary, approachable, visible,
  bigger, context-agnostic, contextual, lasting — ch. 5 acceptance suite.
- **Context-agnostic name:** structure-named ("card"), not context/content-bound ("homepage
  carousel"). Blur test validates.
- **Waterfall vs wax-and-wane:** sequential handoff + signoff theater vs parallel consulting
  throughout with discipline peaks at different times.
- **Sculpture process:** subtractive passes building fidelity; WIP reviews + undo.
- **20-second gut test:** 20–30 sites, 20s each, 1–10 vote on vibe dimensions; top/bottom-5 debate.
- **Ask forgiveness, not permission:** bake system by default when blocked; reveal after delivery.
- **Wine vs used car:** maintained system appreciates; neglected depreciates off the lot.
