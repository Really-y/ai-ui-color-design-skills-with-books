# Examples — before/after cases from Refactoring UI

Compressed illustrations from the book, each with the lesson. Most originals are figures; the
descriptions below come from the surrounding text. Chapter in parentheses.

## Table of contents

1. [Starting from scratch](#starting-from-scratch)
2. [Hierarchy](#hierarchy)
3. [Layout and spacing](#layout-and-spacing)
4. [Text](#text)
5. [Color](#color)
6. [Depth](#depth)
7. [Images](#images)
8. [Finishing touches](#finishing-touches)
9. [Leveling up](#leveling-up)

---

## Starting from scratch

**Flight search before the shell (ch. 1).** Before: trying to "design the app" — top nav vs
sidebar, logo placement, container width. After: design "search for a flight": departure city,
destination city, departure date, return date, search button. Lesson: features inform the shell;
the shell may not even be needed (Google's homepage).

**Grayscale first (ch. 1).** Before: color introduced early to make things pop. After: the same
interface designed in grayscale, hierarchy carried by spacing, contrast and size, then colored.
Lesson: color should enhance an already clear hierarchy.

**Comments with attachments (ch. 1).** Before: comment feature designed with an attachments area
because it will exist "one day"; attachments prove expensive; nothing ships. After: comments
without attachments ship now; attachments later. Lesson: don't imply unbuilt functionality;
design the smallest shippable version.

**Border radius consistency (ch. 1).** Before: square corners mixed with rounded corners in the
same UI. After: one radius policy. Lesson: mixed radii almost always look worse.

**Buttons that are all nearly the same blue (ch. 1).** Before: five candidate button backgrounds
that are visually indistinguishable — no confident choice possible. After: 8–10 predefined
shades with noticeable differences. Lesson: constraints make decisions easy.

**Icon size by elimination (ch. 1).** Scale 12/16/24/32px. Guess 16; compare 12 and 24; both worse
→ 16 wins. If 24 looked better, compare 16/24/32 next.

---

## Hierarchy

**Wall of content (ch. 2).** Before: all elements compete, noisy. After: secondary/tertiary
information de-emphasized, key elements highlighted; colors, fonts and layout untouched. Lesson:
hierarchy, not styling, makes things look designed.

**Bold instead of big (ch. 2).** Before: headline oversized to show importance, metadata tiny.
After: headline bolder at a reasonable size; metadata in a softer grey at readable size.

**Grey on a colored card (ch. 2).** Before: light grey text on a blue panel — reads wrong. Before
(variant): white at 50% opacity — dull, looks disabled, and shows the background image through the
letters. After: a hand-picked lighter/less-saturated blue of the same hue.

**Active nav item (ch. 2).** Before: active item given a different color but still not popping.
After: inactive items made softer; active item now dominant without changes to itself.

**Sidebar vs content (ch. 2).** Before: sidebar with its own background competes with main
content. After: sidebar background removed; content sits on page background.

**Label: value cards (ch. 2).** Before: "Email: janedoe@example.com", "Phone: (555) 765-4321",
"Price: $19.99". After: values alone — format already identifies them. Employee directory:
"Customer Support" under a name needs no "Department:" label. Inventory: "In stock: 12" → "12
left in stock"; real estate: "Bedrooms: 3" → "3 bedrooms".

**Spec sheet (ch. 2).** Scanning for "depth", not "7.6mm": label darker, value slightly lighter —
the reverse of a dashboard, where values dominate and labels are secondary.

**"Manage Account" h1 (ch. 2).** Before: page title huge because it is an h1. After: small title;
the section content is the focus. Lesson: markup for semantics, style for hierarchy.

**Icon next to text (ch. 2).** Before: solid icon in the same dark color as text feels heavier.
After: icon in a softer color. Lesson: lower contrast counterbalances weight.

**1px border (ch. 2).** Before: soft-colored 1px border too subtle; darker color too harsh. After:
2px (heavier) border in the soft color.

**Action buttons (ch. 2).** Before: every action styled as a solid button by its semantics (save,
cancel, delete all bold). After: one solid primary, outline secondary, link-style tertiary; the
delete button is secondary here and becomes big red bold only in its confirmation dialog.

---

## Layout and spacing

**Breathing room (ch. 3).** Before: elements given the minimum space to not look bad. After: much
more space, then trimmed. Lesson: what seems "too much" on one element is "just enough" in the
full UI.

**12→16 vs 500→520 (ch. 3).** A 4px change is +33% for a 12px icon but +4% for a 500px card. Lesson:
scales must be relative, not linear; adjacent values ≥25% apart.

**600px on a 1400px canvas (ch. 3).** Before: content stretched to fill the canvas. After: a 600px
column with generous edge space. Related: not every section must be full-width just because the
nav is.

**Narrow form in a wide page (ch. 3).** Before: form widened to fill, inputs too long. After: form
stays at its optimal width; supporting text moves to a second column — balanced without hurting
usability.

**Grid sidebar (ch. 3).** Before: 3-column (25%) sidebar + 9-column main. Wide screen: sidebar
wastes space; narrow screen: sidebar wraps/truncates. After: fixed-width sidebar, fluid main area
with its own grid.

**Login card (ch. 3).** Before: 6 columns (50%) on large, 8 columns on medium → wider on medium
than large in some viewport range. After: `max-width: 500px`; shrinks only below 500px viewport.

**Headline em ratio (ch. 3).** Before: body 18px, headline 2.5em = 45px; on mobile body 14px →
35px headline, far too large. After: mobile headline 20–24px (1.5–1.7×). Lesson: large elements
shrink faster.

**Button padding (ch. 3).** Before: button sizes derived purely from font size (padding in em) —
feels like zoom. After: large button with proportionally more padding, small button with
proportionally less — feels like genuine size variants.

**Form groups (ch. 3).** Before: equal margin below label and below input; labels float between
fields; users may fill the wrong field. After: larger gap between groups than between a label and
its input. Same lesson for headings close to the preceding paragraph and bullets spaced like
line-height.

---

## Text

**Every size 10–24px (ch. 4).** Before: ad-hoc font sizes everywhere. After: a hand-crafted scale
(see scales-and-systems.md). Related: a 3:4 modular scale gives 12/16/21/28 and you miss 14 and
18.

**em nesting (ch. 4).** 1.25em container (20px) with a .875em child → 17.5px, off-scale. Use
px/rem.

**Google Fonts filter (ch. 4).** Filtering "number of styles" to 10+ removes ~85% of options and
leaves fewer than 50 sans-serifs — a manageable shortlist of well-crafted families.

**Line length (ch. 4).** Before: paragraph stretched across the layout. After: 20–35em width
(45–75 characters) even inside a wider content area holding images.

**Card title + actions (ch. 4).** Before: large title and small action links vertically centered —
visibly misaligned when close together. After: both aligned on the baseline.

**Line-height (ch. 4).** Narrow column at 1.5 reads fine; wide column needs up to 2; large headline
at 1 looks right.

**Link-dense UI (ch. 4).** Before: every link in blue underline, overwhelming. After: links in a
heavier weight/darker color; minor links styled only on hover.

**Centered block too long (ch. 4).** Before: three centered blocks, one wrapping to four ragged
lines. After: copy shortened so all blocks fit 2–3 lines — alignment fixed and design more
consistent.

**Table of numbers (ch. 4).** Before: left-aligned amounts, decimals misaligned. After:
right-aligned; magnitudes comparable at a glance.

**Open Sans vs Oswald (ch. 4).** Open Sans (legible small) used as a headline → tighten letter-
spacing to mimic a headline face. The reverse (Oswald small with added spacing) doesn't work.

**All caps (ch. 4).** Before: uppercase label at default tracking, letters crowd. After: increased
letter-spacing.

---

## Color

**Hex vs HSL (ch. 5).** Two visually related blues look unrelated as hex strings; as HSL they share
a hue and differ only in S/L.

**Five-color generator (ch. 5).** Before: five hex codes from a palette tool. After: greys ×
8–10, primary × 5–10, accents × several — the real requirement for a product UI.

**Alert component as palette test (ch. 5).** The darkest shade (text) and lightest shade
(background tint) of a color are picked together inside an alert, since it uses both.

**Yellow palette (ch. 5).** Before: darkening yellow by lowering lightness yields dull brown.
After: rotate hue toward orange as lightness drops → warm, rich dark yellows. Rotation kept under
20–30°.

**Yellow vs blue at equal lightness (ch. 5).** Same HSL lightness, yellow looks lighter — perceived
brightness peaks at 60°/180°/300°, dips at 0°/120°/240°.

**Cool and warm greys (ch. 5).** Greys tinted blue feel cool; tinted yellow/orange feel warm; the
lightest and darkest greys need extra saturation or they look washed out next to mid greys.

**White badge text (ch. 5).** Before: white text on a colored badge needs a dark background to
reach 4.5:1, so the badge dominates. After: dark shade of the color as text on its light tint —
accessible and quiet.

**Secondary text in a dark panel (ch. 5).** Before: lightening the panel color for text ends up
near white. After: hue rotated toward cyan/magenta/yellow for contrast while staying colorful.

**Red/green metric cards (ch. 5).** Before: trend shown only by color. After: up/down icons added.
Charts: series separated by light vs dark rather than hue alone.

---

## Depth

**Door panel vs cabinet panel (ch. 6).** Raised panel: lighter top edge, darker bottom edge.
Inset panel: shadow at the top, lighter bottom edge. Lesson: light comes from above; mimic it.

**Raised button (ch. 6).** Lighter top edge (top border / inset shadow with slight positive
offset, hand-picked color — translucent white desaturates) + small sharp dark shadow below
(blur a couple px, like a wall outlet's shadow).

**Well / text input / checkbox (ch. 6).** Lighter bottom lip (negative-offset inset shadow or
bottom border) + dark inset shadow at the top (positive offset).

**Button / dropdown / modal (ch. 6).** Small, medium, large shadows respectively — attention
follows apparent proximity.

**Drag and press (ch. 6).** Item gains a shadow on mouse-down (pops forward, signals draggable);
button shadow shrinks or disappears on press (sinks).

**Two shadows on one card (ch. 6).** A large soft offset shadow (cast) plus a tight dark one
(ambient). The tight one fades at higher elevations — try lifting an object off a desk.

**Flat card (ch. 6).** Lighter than the page background → raised; darker → inset; or a solid
offset shadow with no blur.

**Card across two backgrounds (ch. 6).** Card offset so it straddles a colored header and the
white page; element taller than its parent overlapping both edges; carousel controls overlapping
the slide. Overlapping avatars given a background-colored "invisible border".

---

## Images

**Placeholder photos (ch. 7).** Before: beautiful stock placeholders in the mockup, smartphone
shots in production — the design collapses. After: budget for professional or quality stock
photos from the start.

**Hero headline (ch. 7).** Before: no text color works across light and dark regions. After: black
overlay + white text; or lowered image contrast; or colorized image (lower contrast, desaturate,
multiply fill); or glow text-shadow (big blur, no offset).

**Feature icons (ch. 7).** Before: 16–24px icon set scaled 3–4× — chunky, undetailed. After: icon
near native size inside a colored circle/square.

**Screenshot on a landing page (ch. 7).** Before: full desktop screenshot shrunk 70%, 16px text →
4px. After: tablet-layout screenshot in a larger area, a partial crop, or a simplified drawing with
lines standing in for text.

**Favicon (ch. 7).** Before: 128px logo shrunk to 16px — mush. After: simplified redraw at 16px.

**User avatars (ch. 7).** Before: intrinsic aspect ratios break the grid; white-background photos
bleed into the white UI. After: fixed containers with `background-size: cover`; subtle inner
box-shadow (not a border) to hold the shape.

---

## Finishing touches

**Bullets (ch. 8).** Plain bullets → checkmarks/arrows, or padlocks for a list of security features.

**Testimonial (ch. 8).** Quote marks enlarged and colored into a visual element.

**Links (ch. 8).** Thick, colored underline that partially overlaps the text.

**Form controls (ch. 8).** Browser-default checkboxes → brand-colored custom controls; often all
it takes to feel polished.

**Accent borders (ch. 8).** Colored strip on a card's top edge, beside an alert, under a headline,
along the top of the layout, or marking the active nav item.

**Backgrounds (ch. 8).** Section with a different background color; a two-hue gradient (≤30°
apart); Hero Patterns tile at low contrast; a pattern strip along one edge; a few geometric shapes;
a simplified world map.

**Empty state (ch. 8).** Before: feature built with rich sample data; first real user sees a blank
list with tabs and filters that do nothing. After: illustration, encouraging copy, prominent CTA;
supporting UI hidden until content exists.

**Borders everywhere (ch. 8).** Before: every panel and row outlined. After: box-shadows,
alternating background colors, or simply more spacing.

**Reimagined components (ch. 8).** Dropdown as a multi-column panel with icons and descriptions;
table combining "name" and "email" into one cell with hierarchy, plus avatars and colored status;
radio buttons rendered as selectable cards.

---

## Leveling up

**Unexpected decisions (ch. 9).** A datepicker with an inverted background; a button placed inside
a text input; a headline using two colors. Lesson: collect decisions you would not have made.

**Rebuild without dev tools (ch. 9).** Recreating a favorite UI reveals why yours differs: reduced
heading line-height, letter-spacing on uppercase, combined shadows.
