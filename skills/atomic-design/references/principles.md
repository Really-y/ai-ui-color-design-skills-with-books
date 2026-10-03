# Principles — distilled by chapter

Each entry: Frost's point → why it matters → pitfall. Details live in
methodology.md / patternlab.md / playbook.md.

## Ch. 1 — Designing Systems (pp. 8–37)

1. **Page metaphor is user-helpful, builder-harmful.** CERN document roots explain
   bookmarks/pagination; but "page as uniform isolated quantifiable thing" collapses
   on a fluid interdependent medium. Pitfall: homepage estimates, page-count math.
2. **Future-Friendly modularity.** Ford interchangeable parts → OOP separation of
   concerns / single responsibility → YUI/jQuery UI → now mandatory under device
   explosion ("Disruption will only accelerate"). Pitfall: treating modularity as trend.
3. **Big redesigns hurt users and orgs.** Spool's Magic Escalator (relearning cost)
   + New-And-Shiny → Old-And-Crusty without process change. Answer: MVP, ship often.
4. **Agile vs agile (Harned).** Adopt behaviors (cross-discipline, final environment
   fast, ship early, small chunks) and declare what you will be; don't chant slogans.
5. **Team Chunk content.** Well-structured chunks (McGrane) + COPE (NPR) → publish
   everywhere (phones → dashboards). CMSs evolving from page-publishers to chunk
   managers. Pitfall: page-shaped copy.
6. **Classy code.** Mature JS patterns; OOCSS/SMACSS/BEM for CSS modularity. Code
   modularity as design enabler, not backend trivia.
7. **Atmosphere before layout (Clarke).** Feel/mood/identity independent of
   arrangement, felt at every size. Tiles/collages (Warren/Mall) save effort, avoid
   premature-layout promises, force goals conversation. Hay: full comps show "what
   the site will never look like."
8. **Systems not pages (Hay).** Lego/Subway-brick question → responsive tenets
   (Marcotte: fluid grids, flexible media, queries) → This Is Responsive patterns
   still need system to deploy them.
9. **Frameworks: speed with sameness risk.** Bootstrap (77k stars/30k forks then):
   tested patterns, fast prototype/MVP, community, freelancer stability — vs jumpsuit
   future (Frost childhood sci-fi), variety loss, discernment need ("tiny Bootstraps"
   per Rupert, not one Bootstrap everywhere).
10. **Style-guide types to house together.** Brand identity (hard-book → digital),
    writing (Economist), voice/tone, code, design principles, implementation.
    Point: one hub, many lenses.
11. **Six benefits (Debenham/Holgado).** Vocabulary ("Blocks Three-Up"), education
    ("systems not pages," snowflake-syndrome cure), empathetic hub (each discipline's
    concerns under one roof), isolated testing ("what exactly is breaking?"), speed
    after upfront cost (MailChimp 4 screens → reuse everywhere), wine-like longevity
    (redesigns reuse buttons/forms/headings).
12. **Five challenges.** Hard sell (quarterly short-termism), time (Crowley: "hard
    part is building the machine"), auxiliary-project trap (first cut; a11y/perf
    fallacy — bake by default), maintenance/governance or trash-can fate (→ ch. 5),
    audience confusion + vague/technical tone + missing context/lineage + spray-of-
    modules structure (→ ch. 2–3 method + tools).

## Ch. 2 — Methodology (pp. 38–62)

13. **Finite elements, infinite UIs.** Chemistry + Duck's HTML periodic table →
    same blocks, endless compositions.
14. **Five concurrent stages.** Atoms → molecules → organisms → templates → pages
    as hierarchy + mental model. Order for explanation, not execution sequence.
15. **Properties condition application.** Hindenburg hydrogen vs inert helium →
    image dimensions, heading sizes constrain use. Document intrinsic properties.
16. **Molecules earn single responsibility.** Search-form story; simplicity → testable,
    reusable, consistent.
17. **Organisms supply context.** Heterogeneous (header) vs homogeneous (product
    grid); sections reusable anywhere their job recurs.
18. **Templates guard content structure.** Skeleton + limits (Time Inc. sizes/lengths);
    Boulton structure-first. Proves whole functions.
19. **Pages prove with reality.** Representative content (Beyoncé "Moving People");
    user truth + signoff truth + feedback into system.
20. **Abstract↔concrete traversal + shared language + platform-agnosticism + analogy
    discipline.** Zoom for fix vs judgment; taxonomy ("Principles/Basics/..." allowed);
    Instagram native proof; stop chemistry at organisms for stakeholders.

## Ch. 3 — Tools (pp. 64–92)

21. **Tool humility.** Pattern Lab's is/isn't; ugly-by-design; backend-agnostic. No
    perfect tool — vet against six qualities (docs/annotations, code, spectrum
    viewport, variations, dynamic content, lineage).
22. **DRY nesting + named instances.** Includes at every level; Mustache sections for
    latchable instances. Renamable folders.
23. **Data split pays four ways.** DRY, ad hoc CMS, backend blueprint, non-dev
    empowerment. Defaults → overrides.
24. **Worst-case design via pseudo-patterns.** `~` inheritance + flags (`isAdmin`);
    "what-if" catalog (avatar/cart/options/chars/user-state/comments/urgency).
25. **Spectrum over devices.** ish. randomized small/medium/large-ish; fluid +
    container mindset; education > bug-hunt.
26. **Code + docs + lineage as system memory.** Right code (Rizzo include-only at
    grail), living Markdown + pinned annotations, contains/where-used trail for QA
    and weeding.

## Ch. 4 — Workflow (pp. 94–141)

27. **People before tools.** Collaboration is the secret; tech is table stakes.
28. **Now is the time; pilot it.** Don't await ideal project or permission slip.
29. **Sell in time/money, prove with inventory.** Hype fades; über-doc persuades.
30. **Lego discipline.** Organized pile beats rummage; hidden organizing still
    delivers visible whole. Forgiveness over permission when change-averse.
31. **Design = access + resilience + flexibility + speed + enhancement + futurism,**
    not aesthetics. Mall + 3-image story reset the room.
32. **Parallel wax-and-wane + frontend-as-design + sculpture iteration + lo-fi
    direction + gut-test atmosphere + browser decisions.** Waterfall's "fantastic,
    but… pop" dies; WIP + undo + conversation live.

## Ch. 5 — Maintenance (pp. 142–181)

33. **Artifact vs product (Curtis).** Guide can trash-can; system needs roadmap/
    backlog/funding. System-first friction (global dropdown fix) beats page hotfix.
34. **Done is a journey (Curtis).** Not project with end but origin of evolving
    product serving products. Sunset-ride vs initiative-hopping both fail.
35. **Official via thing → useful → sanctioned.** Weekend seed + testimonials +
    plan; grassroots persistence if refused.
36. **Makers ≠ users (Bolton).** Birds-eye vs on-ground; both mandatory. Size shapes
    staffing (Salesforce dozen, small-org hat, consultants teach-to-fish).
37. **Govern change or drift.** Nine Qs + office-hours/Slack/state-of-union. Vanilla
    tree; modify/add/remove with one-off-until-second-use + Sass-Deprecate warnings.
38. **Holy grail or friction death (Schleifer: neglect).** Sync library ↔ production;
    bridges (Rizzo/Twig/Drupal/Starter 8) until grail.
39. **Ten makes as acceptance suite.** Official, adaptable, maintainable,
    cross-disciplinary (carousel test), approachable (Yelp home), visible
    (changelog/Material, auto alerts, training/support ladder, public Bat-Signal —
    Bolton joined Salesforce for its guide), bigger (Harmony + native switches),
    agnostic names (blur test), contextual demos + lineage, lasting (wine).
