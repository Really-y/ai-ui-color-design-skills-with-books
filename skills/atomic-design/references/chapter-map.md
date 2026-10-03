# Chapter map — coverage proof + filler log

Book: Brad Frost, *Atomic Design*, 2016. 189 pp. Foreword (Clark/Mall) + 5 chapters +
Thanks + Resources + About. PDF parsed to `/tmp/atomic.txt` (6567 lines).

| Book section | Pages | Skill location |
|---|---|---|
| Foreword: TechCrunch kitchen-table, exploded-bits demo, chemist talk, 1-hour responsive article page, EW/Time Inc. follow-ons | 5–7 | examples.md (motivation only, no rules) |
| Ch. 1 Designing Systems: paginated past, page-cost fallacy, modularity/strategy/process/content/code/visual, frameworks, style-guide benefits/challenges, methodology hunt | 8–37 | SKILL.md rules 1–7; principles.md §1–12; methodology.md (scope); playbook.md §1–2 |
| Ch. 2 Methodology: chemistry, 5 stages, part/whole, language, native proof, templates vs pages, content-structure | 38–62 | SKILL.md rules 8–15; methodology.md (full); principles.md §13–20; examples.md Ch.2 |
| Ch. 3 Tools: Pattern Lab is/isn't, nesting/includes, Time Inc. chain, data.json→page JSON, pseudo-patterns, ish., code view, annotations, lineage, 6 qualities | 64–92 | SKILL.md rules 16–24; patternlab.md (full); principles.md §21–26 |
| Ch. 4 Workflow: people/process, when to start, pitching, 5-step inventory, forgiveness/Lego, reset (redefine design, waterfall death, dev-is-design, sculpture, direction, gut test, comps) | 94–141 | SKILL.md rules 25–35; playbook.md §1–4; principles.md §27–32 |
| Ch. 5 Maintenance: artifact vs product, done, official (3 moves), makers/users, adaptable governance + 3 changes, maintainable grail, 10 makes (official/adaptable/maintainable/cross-disciplinary/approachable/visible/bigger/agnostic/contextual/last) | 142–181 | SKILL.md rules 36–43; playbook.md §5; principles.md §33–39 |
| Thanks & Acknowledgements (wife Melissa, Olsen/Muenzenmeyer, Clark/Mall/Brook, Gregory/Andrew/Sager, Debenham, Snook, Hay, Clarke, Rupert et al., Zeldman/Meyer/Thiele/Friedman, community, family) | 182–183 | Not converted — gratitude, no transferable method |
| Resources (URL lists per chapter: scope-components, W3C modularity, YUI/jQuery UI, Future-Friendly, Spool, Agile/Scrum/Lean, Harned, McGrane/COPE, JS patterns, OOCSS/SMACSS/BEM, tiles/collages, Hay, Marcotte, This Is Responsive, Foundation/Bootstrap, styleguides.io, Material, voice/tone, Debenham, Holgado, Duck, MDN, SRP, Boulton, Pattern Lab docs, Mustache, container queries, ish., Rizzo, content inventory, Slides template, Nagel, post-PSD, waterfall, dev-is-design, mobile-first, gut test, CodePen, Curtis, Salesforce model, Vanilla, Sass Deprecate, Airbnb, holy-grail, Drupal/Twig, Starter 8, USWDS, Shyp) | 184–190 | Not copied as rules; live links rot (2016). Kept as provenance — consult book for originals |
| About the Author + back-cover blurbs (Zeldman, Coyier) | 191–192 | Not converted |

## Filler / repetition deliberately not skill-ified

- Foreword TechCrunch war story + "whirling dervish / six continents / Antarctica"
  color (pp. 5–7): motivational, no method. Kept as one-line provenance.
- Book/page nostalgia ("razor-sharp pages," clay slabs → scrolls → papyrus) + CERN
  history extended telling: reduced to one-line page-metaphor origin in rule 1.
- Sci-fi jumpsuit illustration + "fashion solved" riff: kept only as framework-sameness
  shorthand, not a rule.
- Bootstrap GitHub star/fork counts, iPhone 4 (320/480) + iPad (768) device widths,
  Jeopardy-music joke, Hindenburg aside, dog joke to Clarke: period color / humor,
  not method. Counts flagged as snapshots where cited.
- Repeated refrains ("show don't tell," "make a thing / show useful / make official,"
  Lego piles, wine vs used car, sculpture): intentionally stated once per context in
  playbook, not duplicated per occurrence. Repetition is Frost's pedagogy, not new rules.
- Image-only spreads (devices collage, tiles, Bootstrap screenshot, Gap grid, Time Inc.
  template/page side-by-side, Pattern Lab dashboards, ish. viewports, Rizzo/Lightning
  code, annotation/lineage screenshots, Lego diagrams, device-evolution triptych,
  Vanilla tree, Yelp/Material/Harmony screenshots): content captured via surrounding
  text + examples.md descriptions; no visual detail invented.
- Thanks/Resources/About: logged above, excluded by design (user principle: practical
  value only).

## Independence note

No concepts imported from Refactoring UI, Albers, Krug, Norman, Garrett, or external
Atomic Design commentary. Where Frost cites others (Hay, Mall, Warren, Clarke,
Marcotte, Spool, Harned, McGrane, Boulton, Debenham, Holgado, Curtis, Bolton,
Schleifer, Nagel, Persson), attribution stays inline so the origin (Frost's use of
that source) is traceable. Tool versions (Pattern Lab PHP/Node, Mustache, data.json)
are Frost-2016 as-written, not updated to current docs.
