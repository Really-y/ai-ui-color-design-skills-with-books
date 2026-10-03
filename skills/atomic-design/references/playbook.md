# Playbook — inventory → workflow → maintenance

Executable steps from ch. 4 (pp. 94–141) and ch. 5 (pp. 142–181). Times, roles, and
scripts are Frost's; adapt names to your org but keep the order.

## 1. Interface inventory (sell + scope in one exercise)

**Purpose:** capture every unique pattern + inconsistency; get buy-in (CEO-cry
über-doc); establish scope (effort per pattern in responsive world); seed the
library + shared vocabulary.

**Step 1 — Round up troops (cross-disciplinary).** Designers, developers, product,
content, even execs. Diversity is the persuasion: everyone sees the 37 buttons.

**Step 2 — Prepare capture.** Everyone uses same software (consistency > tool
choice; Slides works as free-form canvas). Leader pre-defines categories — adapt to
your UI, Frost's bank-site set: buttons, form elements, navigation, media/blocks,
tables/lists, feedback/messages, plus invisible tracking scripts excluded from
screenshots but noted. Share template deck.

**Step 3 — Screenshot sprint (30–90 min, timer on, upbeat music).** Each person
(or pair) owns 1–2 categories. Capture everything the org manages — core flows AND
support/FAQ/sizing/404/legal/terms. Homepage favoritism is the failure mode;
users perceive one brand, not your org chart. Dig deep, no rabbit holes past timer.

**Step 4 — Present (5–10 min per category after a break).** Rationale per pattern,
naming collisions surfaced ("utility bar" vs "admin nav" vs "floating action area"
for same thing; unnamed patterns named). No need to finalize names in 10 min —
open the discussion. Leader merges all decks into one über-document.

**Step 5 — Regroup to next steps (small working group).** Show über-doc to
stakeholders (non-designers get it instantly: 37 buttons = problem). Then answer:
which stay / go / merge? Settled names? Gaps needing second audit? Path from
inventory to living library? If refused funding → §2 fallback.

**Benefits to cite when pitching:** captures inconsistencies side-by-side; buys
org buy-in; scopes work (content/design/dev per component, responsive difficulty);
grounds the future library + vocabulary.

## 2. When blocked — ask forgiveness, not permission

- Bake the system by default like performance/a11y/responsiveness. Don't offer
  "system: yes/no?" — offered nos get taken.
- Mental image (Nagel, Multiscreen UX Design): rummage-pile Lego (dive in, sift
  for each brick) vs organized-pile (take stock, sort, then build deliberately
  faster). Second costs planning, pays in method + time.
- Stakeholders see whole progressing; parts-organizing is your craft choice. Reveal
  after on-time/on-budget launch ("we built a library so we collaborated faster") —
  hard to argue with, parlay into official initiative. Prefer blessing, but don't
  let resistance stop best practice.

## 3. Reset expectations before building

- **Redefine design:** beyond visual aesthetics to accessible/resilient, flexible
  layouts, performance-as-design (respect users' time), progressive enhancement
  (core → layered enhancements), future-friendly, plus ergonomics/input/508/
  legibility per project. Mall: "sell beautiful easy access to content, agnostic of
  device," not paintings. Show 3-image story: desktop-only past → today's
  potpourri (phones/tablets/TVs/consoles/dashboards) → tomorrow's unknown.
- **Kill waterfall:** giant UX PDF → signoff → Photoshop/Sketch comps → projector
  review → "fantastic, but… make it pop" floodgate → deflated designer reworks →
  dev inherits surprises. Replace with parallel wax-and-wane: bulk UX early, bulk
  visual mid, bulk code late, but everyone consults throughout. Draw the two
  timelines; get explicit comfort with blur + WIP reviews.
- **Development is design:** HTML/CSS/presentational JS *are* the UI designers draw.
  Don't seat frontend with middleware/DB work. Browser early to confront
  flexibility, network, interaction, motion, ergonomics, rendering, density, scroll,
  quirks, preferences. Pair static atmosphere + browser prototype — right tool for
  right articulation.
- **Sculpt, don't assemble:** subtractive sculpture (slab → crude shape → face →
  arms → legs, stepping back each pass; we have undo). Build fidelity in loops.
  Name the mess: fuzzy/chaotic collaboration held by honest conversation + tight
  feedback, not Gantt precision.

## 4. Establish direction lo-fi first

- **Content/display patterns (UX-led):** start bulleted IA + conversation ("right
  things? right order?"), then grayscale mobile-first blocks (Food Bank homepage —
  crude but enough to debate hierarchy). Define site-wide gestural display patterns
  without layout/function (TechCrunch "featured island" — "shows content somehow").
  Cheapest articulation: spreadsheet columns (template | display pattern | content
  pattern | order | role). Read left column vertically = mobile-first view.
- **Visual direction:** 20-second gut test at kickoff — 20–30 sites (industry +
  inspirational outsiders, client logo photoshopped in), 20s each, 1 (quit-and-cry)
  to 10 (ecstatic) on type/color/density/illustration/vibe; tally, discuss bottom-5
  + top-5. Follow with style tiles / element collages for atmosphere (no layout).
  Never 10 full comps to "see what sticks."
- **Comps as hypotheses:** static = atmosphere proposal; browser = decision venue
  for responsive behavior, states, motion. Post-PSD era: Pattern Lab header included
  via `{{> organisms-header }}` everywhere — fix once, propagate.

## 5. Make it last — the ten "make it ..." (ch. 5 checklist)

1. **Official:** weekend-hackathon seed → package for show → prove time/money +
   testimonials + scaled vision → sanction (people/budget/governance/roadmap).
   If no, grow grassroots until undeniable.
2. **Adaptable:** governance answers nine Qs (modify vs swap vs create; new
   requests; retirement; bugs; approver; docs owner; coder; deploy; announce).
   Vanilla decision-tree for additions; assume one-off until second "I want that!"
3. **Maintainable:** reduce update friction (tech + workflow) or neglect kills
   (Schleifer). Chase holy grail (library ↔ production sync: Rizzo/Twig/Drupal,
   Starter 8) so one edit updates both.
4. **Cross-disciplinary:** makers (create/govern: Salesforce ~dozen FTE; small org
   senior hat; consultants teach-to-fish) + users (apply/report: same team → global
   strangers). Hands (UX/visual/frontend) vs advisors (backend/exec/users).
   House carousel-scale concerns (business/editorial/copy/art/UX/frontend/backend)
   on one pattern page.
5. **Approachable:** attractive navigable home stating what/who/how (Yelp model).
   Usefulness first, gloss after official — but gloss signals commitment.
6. **Visible:** evangelize pre-launch (blog/Yammer); communicate change
   (changelog — Material model; roadmap; success stories; tips) where teams live
   (Slack/Basecamp/GitHub/wiki/email/intranet) + auto alerts (PR → #Design);
   train (pair > workshop > webinar > tutorial > onboarding) + support (JIRA/GitHub
   issues, office hours, chat, forum, proactive outreach, PRs, interviews,
   feedback-asks, surveys, state-of-union recorded).
7. **Bigger:** co-house brand/voice/code/principles/writing (Harmony model) +
   native iOS/Android switches beside web — one watering hole.
8. **Context-agnostic (names):** "carousel"/"card" not "homepage carousel"/
   "product card"; blur-content naming exercise; structure-named = portable.
9. **Contextual (usage):** photos/videos of use (Material) + lineage paper trail
   (contains + where-used) for QA scope.
10. **Last (wine not used car):** governance + communication + care compound;
    even ground-up rebuilds reuse buttons/fields/tabs — don't throw baby with
    bathwater. "Go forth and be atomic."
