# Playbook — task-oriented procedures from Refactoring UI

Organized around the authors' chapters. Each section: when you are doing X → steps, checks and
decision rules. Chapter attributions in parentheses. For the numbers behind each rule see
scales-and-systems.md; for the reasoning see principles.md.

## Table of contents

1. [Starting from scratch — new product, feature, or screen](#1-starting-from-scratch--new-product-feature-or-screen)
2. [Hierarchy — making a screen read correctly](#2-hierarchy--making-a-screen-read-correctly)
3. [Layout and spacing](#3-layout-and-spacing)
4. [Designing text](#4-designing-text)
5. [Working with color](#5-working-with-color)
6. [Creating depth](#6-creating-depth)
7. [Working with images](#7-working-with-images)
8. [Finishing touches](#8-finishing-touches)
9. [Leveling up — improving your eye](#9-leveling-up--improving-your-eye)
10. [Symptom → diagnosis → fix table](#10-symptom--diagnosis--fix-table)

---

## 1. Starting from scratch — new product, feature, or screen

### 1.1 When kicking off a new app or feature design (ch. 1)
1. Pick one real feature, not the shell. Write down the minimum UI it needs (fields, buttons,
   outputs) and design only that.
2. Work low fidelity first: paper + thick marker or a rough wireframe. Defer typeface, shadow and
   icon decisions. Throw the sketches away once the decision is made.
3. Move to higher fidelity **in grayscale**. Create hierarchy with spacing, size and contrast
   only. Add color last.
4. Ship in cycles: design the simple version → build it for real → fix problems in the working UI
   → design the next feature. Do not pre-design every edge case.
5. Be a pessimist: strip anything you are not ready to build (no "attachments" area on a comment
   box you won't implement now). Define the smallest useful version and keep nice-to-haves for a
   later cycle.

### 1.2 When choosing a personality / look (ch. 1)
1. Decide the register: serious/professional vs playful/friendly. If unsure, review sites your
   audience already uses and match their register (without copying direct competitors).
2. Set the four levers consistently:
   - typeface: serif (elegant), rounded sans (playful), neutral sans (plain);
   - a primary color: blue (safe), gold (expensive), pink (fun), etc.;
   - one border-radius policy for the whole UI: none (formal), small (neutral), large (playful);
   - copy tone: formal vs casual.
3. Check consistency: no mix of square and rounded corners; tone of microcopy matches the visuals.

### 1.3 When setting up a project's design systems (ch. 1, 3, 4, 5, 6)
Define, in this order, before designing many screens:
1. Spacing/sizing scale (16px base, non-linear, ≥25% steps).
2. Type scale (hand-picked px/rem values).
3. Font weights (two: 400/500 and 600/700) and text color roles (dark, grey, light grey).
4. Grey scale (8–10 shades, no true black), primary color shades (5–10), accent shades.
5. Shadow/elevation set (about five).
6. Border radius policy, border widths, opacities as needed.
Then, for any further "12px or 13px?" moment, add a system rather than deciding ad hoc. Pick values
by elimination (guess, compare neighbors, repeat).

---

## 2. Hierarchy — making a screen read correctly

### 2.1 When a screen feels noisy, flat or "undesigned" (ch. 2)
1. Classify every element as primary, secondary or tertiary.
2. De-emphasize secondary/tertiary before emphasizing primary: softer color, smaller size, lighter
   weight, removed backgrounds.
3. Use at most 2–3 text colors and 2 weights across the screen.
4. If something still doesn't stand out, do not add more to it — tone down what competes with it
   (soften inactive nav items; remove a sidebar's background).
5. Check icons: solid icons are heavy; give them a softer color than adjacent text.
6. Check thin borders: if a soft 1px border is too faint, widen it rather than darkening it.

### 2.2 When controlling emphasis for text (ch. 2)
- Primary → heavier weight (600/700) at a sensible size, dark color.
- Secondary → grey color at normal size (not tiny).
- Tertiary → lighter grey, possibly smaller.
- Never go below weight 400 for small text; never de-emphasize with a thin weight.
- On a colored background: pick the same hue, adjust saturation/lightness; do not use grey and do
  not use white at reduced opacity (dull, looks disabled, lets backgrounds show through).

### 2.3 When displaying data records (ch. 2 "Labels are a last resort")
Decision ladder for each field:
1. Does the format identify it (email, phone, price)? → no label.
2. Does context identify it (department under a name)? → no label.
3. Can the label fold into the value ("12 left in stock", "3 bedrooms")? → do that.
4. Must it be scannable among many similar fields (dashboard)? → keep label, make it secondary
   (smaller, lower contrast, lighter weight).
5. Will users scan for the *label* (spec sheets)? → emphasize the label (darker), value slightly
   lighter — but keep the data readable.

### 2.4 When styling headings in an application UI (ch. 2)
- Choose h1/h2/h3 for semantics; size them for hierarchy. Section titles usually act as labels:
  small, supportive. Consider visually hidden headings when the content is self-explanatory.

### 2.5 When designing a set of actions/buttons (ch. 2 "Semantics are secondary")
1. Identify the single primary action on the page.
2. Primary: solid high-contrast fill. Secondary: outline or low-contrast fill. Tertiary: link style.
3. Destructive actions that are not primary here → secondary/tertiary; move the big red bold
   button to the confirmation dialog where it is the primary action.

---

## 3. Layout and spacing

### 3.1 When spacing a component or page (ch. 3)
1. Start with far too much white space; remove until it looks right. Expect to keep more than
   feels natural at first.
2. Use only values from the spacing scale; if a gap is slightly too small, take the next value.
3. Grouping check: space around a group must exceed space within it (form label ↔ input closer
   than input ↔ next label; more space above a heading than below it; bullet gaps larger than the
   bullet's line height; same rule horizontally).
4. If deliberately dense (dashboard), make that an explicit decision and keep the grouping rule.

### 3.2 When deciding widths (ch. 3)
1. Give each element the width its content needs; do not stretch to fill 1200–1400px canvases.
   Sections need not be full-width because the nav is.
2. Fixed vs fluid: sidebars, cards, forms → fixed or `max-width`; main content → flexes. Use
   percentages only where scaling is desired, including inside components.
3. Login/card pattern: set `max-width` (e.g. 500px) and let it shrink only below that viewport
   width — never size with grid columns that make it narrower on large screens than on medium.
4. Narrow form in a wide layout → add a side column (helper text) instead of widening the form.
5. Don't cram either: use the space you need.

### 3.3 When designing responsive behavior (ch. 3 "Relative sizing doesn't scale")
1. Design at ~400px first, then expand; fix only what felt compromised.
2. Shrink large elements faster than small ones: desktop headline 45px/body 18px (2.5×) → mobile
   headline 20–24px/body 14px (1.5–1.7×). Do not encode this as a fixed em ratio.
3. Component variants: tune padding per size (large buttons get relatively more padding, small
   buttons relatively less); don't derive padding from font-size.

---

## 4. Designing text

### 4.1 When defining typography for a project (ch. 4)
1. Type scale: hand-pick px/rem sizes (see scales-and-systems.md); never em for the scale.
2. Choose a typeface: neutral sans-serif or the system stack if unsure; reject families with < 5
   weights (Google Fonts "styles ≥ 10" filter); avoid condensed/short-x-height faces for body UI;
   sort by popularity; borrow from well-designed sites.
3. Weights: two (400/500 normal, 600/700 bold).

### 4.2 When styling paragraphs and long text (ch. 4)
- Width 20–35em → 45–75 characters per line; keep it even when images/components are wider.
- Line-height: ~1.5 for narrow text, up to 2 for wide; smaller text gets taller line-height; large
  headlines ~1.
- Left-align by default. Center only short blocks (≤ 2–3 lines); shorten copy if a centered block
  wraps too much.
- Justified text → enable hyphenation (and consider left-align anyway).

### 4.3 When laying out mixed sizes, tables, links, caps (ch. 4)
- Mixed font sizes on one row → align baselines.
- Numeric columns → right-align.
- Link-heavy UIs → emphasize links with weight/darker color, not link-blue; ancillary links get
  hover-only underline/color. Links inside prose must still look clickable.
- All-caps labels → add letter-spacing. Headline set in a body face → tighten letter-spacing; never
  use a headline face at small sizes.

---

## 5. Working with color

### 5.1 When building a palette (ch. 5)
1. Work in HSL (browsers understand it; HSB is for design tools).
2. Inventory needs: greys (8–10 shades), 1–2 primaries (5–10 shades), accents for attention,
   semantic states (red/yellow/green) and categories (charts, calendars, tags). Up to ~10 colors.
3. For each color: pick base (500) as a good button background → pick 900 (text) and 100
   (background tint) by testing in an alert component → fill 700/300 → fill 800/600/400/200.
4. As lightness moves away from 50%, increase saturation so ends don't wash out; for light colors
   such as yellow, rotate hue toward the nearest dark hue (orange/red direction) when darkening,
   within 20–30°.
5. Greys: pick darkest text and lightest off-white first; tint all greys slightly blue (cool) or
   yellow/orange (warm); boost saturation at both ends to keep the temperature even. No true black.
6. Freeze the set; tweak by eye after use; don't add shades casually; never lighten()/darken()
   on the fly.

### 5.2 When text must sit on a colored surface (ch. 2, ch. 5)
- Secondary text on a colored background: same hue, adjusted saturation/lightness (not grey, not
  translucent white).
- Need 4.5:1 with white text? If the required dark background over-emphasizes a non-focal element,
  flip: dark shade of the color as text on the 100-level tint as background.
- Colored-on-colored (e.g. secondary text in a dark panel): rotate the text hue toward cyan,
  magenta or yellow to gain contrast without going white.

### 5.3 When using color to convey meaning (ch. 5)
- Add a second channel: icons/arrows for positive vs negative, labels for status.
- Multi-series charts: separate series by lightness/contrast, not hue alone.

---

## 6. Creating depth

### 6.1 When an element should look raised or inset (ch. 6)
1. Decide the profile (raised vs recessed) and remember light comes from above; viewers look
   slightly down.
2. Raised: lighter top edge (top border or inset shadow, slight positive y-offset, hand-picked
   color) + small dark shadow below (slight y-offset, blur of a couple px).
3. Inset: lighter bottom edge (bottom border or inset shadow, negative y-offset) + small dark inset
   shadow at the top (slight positive y-offset).
4. Stop before it looks photo-realistic.

### 6.2 When assigning shadows across the UI (ch. 6)
1. Define about five shadows from smallest to largest, growing roughly linearly.
2. Assign by z-position: buttons small, dropdowns medium, modals large. The closer to the user,
   the more attention it draws — use that deliberately.
3. For polish use two-part shadows: a soft offset cast shadow plus a tight dark ambient shadow;
   weaken the ambient part as elevation increases.
4. Tie shadows to interaction: lift on drag start, sink (smaller/no shadow) on button press.

### 6.3 When the style is flat (ch. 6)
- Lighter than background = raised; darker = inset. Optionally a solid shadow (short y-offset,
  no blur).

### 6.4 When a layout feels flat and boxed-in (ch. 6)
- Overlap: let a card straddle two background regions; make an element taller than its container;
  overlap controls over images. Give overlapping images an "invisible border" in the background
  color.

---

## 7. Working with images

### 7.1 When the design needs photography (ch. 7)
- Hire a professional for specific shots or use high-quality stock (Unsplash). Never design with
  placeholders intending to shoot phone photos later.

### 7.2 When text sits on a photo (ch. 7)
Pick one or combine, in order of control:
1. Semi-transparent overlay: black under light text, white under dark text.
2. Reduce the image's contrast; re-adjust brightness.
3. Colorize: reduce contrast → desaturate → solid brand-color fill with multiply blend.
4. Text shadow as a glow (large blur, no offset) to add contrast only where needed; still lower
   image contrast a little.

### 7.3 When placing icons, screenshots and logos (ch. 7)
- Need large icons but only 16–24px ones? Keep them near native size inside a colored shape.
- Need a screenshot in a small area? Capture at a smaller layout (tablet), crop to a partial view,
  or draw a simplified mock with lines for text. Never shrink a full desktop screenshot ~70%.
- Favicons/small logos: redraw simplified at 16px; don't downscale a 128px asset.

### 7.4 When users upload images (ch. 7)
- Fixed-size containers, centered and cropped (`background-size: cover`).
- Prevent bleed with a subtle inner box-shadow or semi-transparent inner border, not a solid
  border.

---

## 8. Finishing touches

### 8.1 When a design is correct but plain (ch. 8)
Try, roughly in order of effort:
1. Supercharge defaults: icon bullets (check, arrow, padlock), oversized colored quote marks,
   custom link underlines, brand-colored checkboxes/radios.
2. Accent borders: top of cards, active nav, alert side, under headlines, top of the layout.
3. Backgrounds: change color per panel/section; gradient of two hues ≤30° apart; subtle repeating
   pattern (full or along one edge); a shape, pattern fragment or simplified map at low contrast.
4. Rethink components: dropdowns with sections/columns/icons; tables merging related non-sortable
   columns, adding images/color; radio groups as selectable cards.

### 8.2 When a design feels busy (ch. 8 "Use fewer borders")
Replace borders with: a box-shadow (if element color ≠ background), distinct background colors
(drop the border if both exist), or more spacing.

### 8.3 When a feature depends on user content (ch. 8)
Design the empty state first-class: illustration + emphasized CTA; hide tabs/filters/supporting UI
until there is content.

---

## 9. Leveling up — improving your eye

- When you admire a design, name the decisions you wouldn't have made (inverted datepicker,
  button inside an input, two-tone headline) and store them as techniques.
- Rebuild a favorite interface from scratch without dev tools; the gaps between your copy and the
  original expose tricks (tight heading line-height, caps letter-spacing, layered shadows).

---

## 10. Symptom → diagnosis → fix table

| Symptom | Likely cause (chapter) | Fix |
|---|---|---|
| Everything looks equally important; "wall of content" | No hierarchy (2) | Classify primary/secondary/tertiary; de-emphasize the lower levels first |
| Headlines huge, helper text unreadable | Size-only hierarchy (2) | Use weight + color; 2–3 colors, 2 weights |
| Light text on colored card looks disabled | Grey/translucent white on color (2) | Same-hue color with adjusted S/L |
| Active nav item doesn't stand out | Competitors too strong (2) | Soften inactive items |
| Dashboard reads as "label: value" soup | Labels everywhere (2) | Drop/merge labels; secondary styling for the rest |
| h1 dominates an app page | Document hierarchy drives size (2) | Make the title small; content is the focus |
| Icons shout next to text | Heavy surface area (2) | Lower icon contrast |
| Soft borders invisible, dark ones harsh | Weight/contrast imbalance (2) | Widen the border, keep the soft color |
| Too many bold buttons | Semantics-driven buttons (2) | One primary, outline secondaries, link tertiaries; red only in confirmation |
| Cramped, cluttered | Minimum white space (3) | Start with too much space, remove to taste |
| Inconsistent gaps | No spacing scale (3) | 16px-based non-linear scale, ≥25% steps |
| Unsure which label goes with which input | Ambiguous spacing (3) | More space around groups than within |
| Wide screens feel sparse and hard to scan | Filling the canvas (3) | Use needed width; max-widths; columns |
| Sidebar too wide on large / cramped on small | Fluid grid (3) | Fixed sidebar width, fluid main |
| Mobile headlines oversized | em ratios (3) | Independent sizes per breakpoint |
| Lines hard to follow, lines skipped | Line length / line-height (4) | 45–75 chars; taller line-height for wide/small text |
| Centered paragraph looks ragged | Centered long text (4) | Left-align or shorten |
| Numbers hard to compare | Left-aligned numerals (4) | Right-align |
| Uppercase label hard to read | Default tracking (4) | Add letter-spacing |
| Link-blue everywhere | Prose link style in app UI (4) | Weight/darker color; hover-only for ancillary |
| 35 slightly different blues | On-the-fly shades (5) | Fixed 100–900 scale |
| Light tints look washed out | Saturation lost at high lightness (5) | Raise saturation at the ends; rotate hue toward bright hues |
| Dark shades look muddy/brown | Lightness-only darkening (5) | Rotate toward 0°/120°/240°, ≤20–30° |
| Greys feel lifeless or mismatched | 0% saturation / inconsistent temperature (5) | Tint greys; boost saturation at ends |
| Accessible badge is too loud | White on dark color (5) | Flip contrast: dark text on light tint |
| Colorblind users can't read status | Color-only (5) | Icons/contrast as a second channel |
| Shadows look fake or random | No elevation logic (6) | Five-step system; z-position decides; two-part shadows |
| Flat design feels lifeless | No depth cues (6) | Lighter = closer; solid shadows; overlap elements |
| Hero text unreadable | Image dynamics (7) | Overlay / lower contrast / colorize / glow shadow |
| Feature icons look chunky | Upscaled 16–24px icons (7) | Native size inside colored shape |
| Screenshot illegible | Downscaled full screenshot (7) | Tablet-size capture, partial, or simplified drawing |
| Avatars break the grid / bleed | Intrinsic sizes, matching bg (7) | Fixed crop containers; inner shadow |
| Design is correct but boring | No finishing touches (8) | Icon bullets, accent borders, background decoration, rethink components |
| Busy with lines everywhere | Border overuse (8) | Shadows, background colors, spacing |
| New feature looks broken on first open | Empty state ignored (8) | Illustration + CTA; hide inert controls |
