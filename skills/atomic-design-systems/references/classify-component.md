# Classifying a component: atom, molecule, organism, template or page (Frost, ch. 2 and ch. 3)

A decision guide for assigning a UI pattern to one of the five atomic design stages, with Frost's
definitions, his examples, and edge cases. Remember the framing caveat first: atomic design "is not a
linear process, but rather a mental model" — classification exists to give the library hierarchy and
a shared vocabulary, not to be defended as dogma. If your organization uses other labels (GE:
Principles, Basics, Components, Templates, Features, Applications), map them and move on.

## Contents

1. The definitions in one table
2. The decision procedure (questions in order)
3. Signals for each stage
4. Worked examples from the book
5. Edge cases and judgement calls
6. Naming the thing you just classified
7. What to record for each pattern

---

## 1. The definitions in one table

| Stage | Frost's definition (ch. 2) | Test |
|---|---|---|
| Atom | basic HTML elements (labels, inputs, buttons...) "that can't be broken down any further without ceasing to be functional"; each has intrinsic properties (hero image dimensions, primary heading font size) | Remove any part and it stops being a functional UI element? -> atom |
| Molecule | "relatively simple groups of UI elements functioning together as a unit"; "do one thing and do it well" (single responsibility) | Two or more atoms that together gain one purpose? -> molecule |
| Organism | "relatively complex UI components composed of groups of molecules and/or atoms and/or other organisms. These organisms form distinct sections of an interface." | Would you point at it on a page and call it a section (header, footer, product grid, comment thread)? -> organism |
| Template | "page-level objects that place components into a layout and articulate the design's underlying content structure" | Is it a whole screen's layout with placeholder content and content rules (image sizes, character lengths)? -> template |
| Page | "specific instances of templates that show what a UI looks like with real representative content in place" | Same layout, real content, or a specific variation (admin, empty state, long headline)? -> page |

## 2. The decision procedure

Ask in this order; stop at the first "yes".

1. **Is this a whole screen with real or representative content, or a named variation of a screen
   (admin vs user, 1 item vs 10, first-time vs returning)?** -> **Page.** (Pages are instances of
   templates; in Pattern Lab a variation is a pseudo-pattern such as `dashboard~admin.json`.)
2. **Is this a whole screen's layout showing content structure — grey FPO images with dimensions,
   lorem text with character limits — rather than real content?** -> **Template.**
3. **Is it a distinct, standalone section of an interface** (you could draw a box around it and label
   it "header", "footer", "product grid", "photo stream item", "story feature"), **made of molecules
   and/or atoms and/or other organisms?** -> **Organism.**
   - Same molecule repeated (product grid of product-item molecules; a stream of photo organisms) ->
     still an organism.
   - Different molecules combined (logo + primary nav + search) -> organism.
4. **Is it a small group of atoms that together do one job** (label + input + button = search form;
   thumbnail + headline + excerpt = block; icon row = actions bar)? -> **Molecule.**
   - If it is trying to do several jobs, it is probably an organism or it should be split into
     molecules (single responsibility).
5. **Is it a single element you cannot decompose without it ceasing to function** (button, input,
   label, heading, icon, image, colour, type style)? -> **Atom.**

If none fits cleanly, see section 5 and pick the stage that gives the most useful hierarchy for your
library — then document the decision.

## 3. Signals for each stage

**Atom signals**
- Maps to one HTML element (or one visual primitive: a colour, a font size, an icon glyph).
- Has intrinsic properties worth documenting on their own: dimensions, font size, colour.
- Appears in the library mainly to "demonstrate all your base styles at a glance".
- Does not make sense in isolation to a user ("don't exist in a vacuum and only really come to life
  with application").

**Molecule signals**
- "When combined, these abstract atoms suddenly have purpose": the label now defines the input; the
  button now submits the form.
- Portable: "can be dropped in anywhere search functionality is needed".
- Simple enough to test in isolation and reason about quickly.
- Variation is expressed by data (an `isAdmin` flag adding an actions molecule), not by duplicating
  the pattern.

**Organism signals**
- A "standalone section of an interface, even though it contains several smaller pieces ... with their
  own unique properties and functionality".
- Is the thing people name when describing a page ("the header", "the product grid", "the sidebar").
- Reusable across several templates (product grid: category listings, search results, related
  products).
- Can include other organisms.
- Pattern Lab lineage shows multiple molecules/atoms inside it and several templates using it.

**Template signals**
- Only "pulls [patterns] into the context of a page layout and give[s] them unique names"
  (`{{# factoid-advertising }}{{> organisms-factoid }}{{/ factoid-advertising }}`); at template stage
  "the smaller patterns are already constructed".
- Shows the content skeleton: image sizes, heading and text character lengths, which areas are
  dynamic (Instagram: handle, avatar, photo, like count, caption).
- Exists to "prove the parts add up to a well-functioning whole" and to give back-end developers a
  blueprint of static vs dynamic parts.

**Page signals**
- Real representative content poured into a template (Time Inc.: "Moving People" + a Beyoncé photo
  replacing "Lorem Ipsum" + grey FPO image).
- The thing stakeholders sign off and users see.
- Used to "test the effectiveness of the underlying design system": if content breaks a pattern, loop
  back and fix the molecule/organism/template.
- Articulates variations: cart with 1 vs 10 items; dashboard with recent activity suppressed for
  first-time users; 40- vs 340-character headline; admin-only buttons.

## 4. Worked examples from the book

| Component | Stage | Why (Frost) |
|---|---|---|
| Form label, search input, button | atoms | basic HTML elements; can't be reduced further |
| Label + input + button | molecule (search form) | "simple, portable, reusable component" |
| Thumbnail + headline + excerpt (Time Inc. `block-post`) | molecule | three atoms working as a single unit; `{{> atoms-thumb }}` inside |
| Logo + primary nav + search form | organism (header) | distinct standalone section; dissimilar molecules |
| Product item repeated in a grid (Gap category page) | organism (product grid) | same molecule repeated; reusable section |
| Media block: image + headline + text + button bar | molecule (media-block) | lineage: contains atoms-square and molecules-button-bar; used by media-block-list organism |
| List of media blocks | organism (media-block-list) | section composed of repeated molecules |
| Instagram: icons, text, primary image, avatar | atoms | |
| Instagram: bottom nav bar, photo-actions bar (like/comment) | molecules | "simple utilitarian components" of several icons |
| Instagram: user info + timestamp + photo + actions + like count + caption | organism (photo) | "cornerstone of the entire Instagram experience", stacked repeatedly |
| Instagram feed layout with exposed dynamic fields | template | content skeleton: handle, avatar, photo, like count, caption |
| Instagram feed with real posts | page | final product with real content |
| Homepage: header, hero, sections, four-item feature, factoid, footer (Time Inc.) | template | organisms and molecules applied to a layout |
| Homepage with "Moving People" headline and real photo | page | representative content |
| Dashboard collaborator list; `dashboard~admin.json` with edit/delete actions | page + variation (pseudo-pattern) | same template, data toggles the actions molecule |

## 5. Edge cases and judgement calls

- **"Is a button with an icon an atom or a molecule?"** Frost's atoms are single HTML elements; an icon
  inside a button is still one functional element (the button). Treat it as an atom variant unless the
  icon and label act as separable parts. (extractor note: the book does not rule on this explicitly;
  decide by the "can't be broken down without ceasing to be functional" test.)
- **Molecule vs organism.** Use *complexity and role*, not element count. A molecule does one simple
  job and is portable; an organism is "relatively complex" and reads as a *section* of the interface.
  If a group has several responsibilities (navigation + search + branding), it is an organism. If a
  pattern is "burdened ... with too much complexity", split it into molecules so testing, reuse and
  consistency improve.
- **Repetition does not change the stage.** One product item is a molecule; the grid of them is an
  organism (same for a photo organism repeated in a stream — the repeated unit was already an organism
  because of its internal complexity).
- **Organisms inside organisms** are allowed by definition ("and/or other organisms"), e.g. a header
  organism inside a page-shell organism. Don't invent a sixth level; nest.
- **The "section vs molecule" grey zone (e.g. a card with image, title, text, button).** Frost calls the
  media block a molecule although it has four parts — because it does one thing (summarize an item)
  and is portable. The list of them is the organism. Lean on single responsibility.
- **Templates vs pages when there is no CMS.** Template = structure with FPO content and content
  rules; page = the same with representative content. If you only have one of them, you are missing a
  stage: without templates, nobody documented image sizes and character lengths; without pages, the
  system was never tested against real content.
- **Variations.** Active/disabled tabs, hover/loading buttons, admin views, empty states are *not* new
  patterns; they are variations of one pattern, articulated with data or state (pseudo-patterns, ch.
  3) and shown in the library ("the ability to showcase pattern variations, such as active or disabled
  tabs"). Create a new pattern only when another team says "I want that!" (ch. 5 addition rule).
- **Colours, type scales, spacing.** Frost's inventory treats colours and headings as categories and
  atoms "demonstrate all your base styles". Put them in the atom (or "basics") level.
- **Third-party widgets, ads, iframes.** Inventory them (ch. 4 categories). Classify by role: an ad
  slot is usually an atom-like placeholder with fixed dimensions; a social-share bar is a molecule; an
  embedded comments system is an organism.
- **Stop arguing.** "Naming things is hard and imperfect ... whatever taxonomy you choose ... should
  help you and your organization communicate more effectively." If a debate lasts longer than a few
  minutes, record both views, pick one, and revisit after the pattern has been used in two templates.

## 6. Naming the thing you just classified (ch. 2, ch. 3, ch. 5)

- Name by **structure**, not location ("carousel" not "homepage carousel") and not content ("card" not
  "product card") — agnostic names are "more portable, reusable, and versatile".
- Trick: blur out the content in the screenshot so the name describes the skeleton.
- Prefix or folder by stage if your tool supports it (`atoms-thumb`, `molecules-search`,
  `organisms-header`); labels and folders can be renamed to your taxonomy.
- Names should imply hierarchy to the team (that is the whole argument for atom/molecule/organism).
- Give *instances* their own names in templates (`factoid-advertising`) separately from the pattern
  name (`organisms-factoid`).

## 7. What to record for each pattern

From ch. 2-3 and ch. 5 ("make it contextual"):
- Stage and name; the patterns it contains and where it is used (lineage).
- Content structure it must hold: image sizes, character ranges, optional elements.
- Variations/states and the data that drives them.
- Responsive behaviour across the resolution spectrum (not just 320/480/768).
- Discipline notes: accessibility, performance, copy/tone constraints, back-end wiring.
- Code to include it, and its HTML/CSS/JS as appropriate.
