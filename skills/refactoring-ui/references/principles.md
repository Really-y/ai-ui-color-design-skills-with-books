# Principles and concepts — Refactoring UI

Every principle the authors state, by chapter. Format: name, definition, why, how to apply,
pitfalls. Chapter numbers: 1 Starting from Scratch, 2 Hierarchy is Everything, 3 Layout and
Spacing, 4 Designing Text, 5 Working with Color, 6 Creating Depth, 7 Working with Images,
8 Finishing Touches, 9 Leveling Up.

## Table of contents

1. [Ch. 1 — Starting from scratch](#ch-1--starting-from-scratch)
2. [Ch. 2 — Hierarchy is everything](#ch-2--hierarchy-is-everything)
3. [Ch. 3 — Layout and spacing](#ch-3--layout-and-spacing)
4. [Ch. 4 — Designing text](#ch-4--designing-text)
5. [Ch. 5 — Working with color](#ch-5--working-with-color)
6. [Ch. 6 — Creating depth](#ch-6--creating-depth)
7. [Ch. 7 — Working with images](#ch-7--working-with-images)
8. [Ch. 8 — Finishing touches](#ch-8--finishing-touches)
9. [Ch. 9 — Leveling up](#ch-9--leveling-up)
10. [Glossary of the authors' terms](#glossary-of-the-authors-terms)

---

## Ch. 1 — Starting from scratch

### Start with a feature, not a layout (ch. 1)
- **Definition:** Begin a new design with a concrete piece of functionality, never with the
  application shell (top nav vs sidebar, nav left or right, container vs full-width, logo spot).
- **Why:** An app is a collection of features. Until a few features exist you lack the information
  needed to decide how navigation should work, so starting with the shell is frustrating and
  arbitrary.
- **Apply:** Pick one feature and list the interface it genuinely needs. Flight-booking example:
  "search for a flight" needs a departure-city field, destination-city field, departure date,
  return date, and a search button. Design that. The shell may turn out unnecessary (the authors
  cite Google's homepage).
- **Pitfall:** Designing the chrome first, then forcing features into it.

### Detail comes later (ch. 1)
- **Definition:** In early stages, do not make low-level decisions (typefaces, shadows, icons).
- **Why:** Low fidelity keeps you fast so you can build the real thing sooner; obsessing over
  details is impossible with a thick Sharpie on paper (Jason Fried / Basecamp trick) and that is
  the point.
- **Apply:** Sketch many layout ideas quickly. Treat sketches and wireframes as disposable; users
  cannot do anything with static mockups.
- **Hold the color:** Even when refining in higher fidelity, design in grayscale first so spacing,
  contrast and size carry the hierarchy. It is harder, but the result is a clearer interface that
  is easy to enhance with color later.
- **Pitfall:** Over-investing in mockups; reaching for color to patch a weak hierarchy.

### Don't design too much (ch. 1)
- **Definition:** Do not design every feature (and every edge case) before implementing.
- **Why:** Edge cases ("2000 contacts", "where does the form error go", "two calendar events at
  the same time") are hard to solve in the abstract with only a design tool and imagination.
- **Work in cycles:** design a simple version of the next feature → make it real → iterate on the
  working interface until no problems remain → return to design mode for the next feature.
  Fixing design problems in something usable beats imagining every edge case up front.
- **Be a pessimist:** never imply functionality you are not ready to build. Example: a comment
  system designed with an attachments section; attachments turn out expensive; the whole feature
  stalls, although comments without attachments would have been better than nothing. Expect every
  feature to be hard; design the smallest useful version you can ship; nice-to-haves come later
  so you always have a fallback.

### Choose a personality (ch. 1)
- **Definition:** Every design communicates a personality (secure/professional vs fun/playful),
  and it is produced by a few concrete factors, not by vague "feel".
- **Factors and the authors' readings:**
  - Font: serif → elegant/classic; rounded sans-serif → playful; neutral sans-serif → plain,
    letting other elements carry the personality.
  - Color: blue → safe and familiar ("nobody ever complains about blue"); gold → expensive,
    sophisticated; pink → fun, not serious. Color psychology alone is not practical; it helps you
    explain why a color feels right.
  - Border radius: small → neutral, says little; large → playful; none → serious/formal.
    Stay consistent: mixing square and rounded corners in one interface almost always looks worse.
  - Language: impersonal tone → official/professional; casual, friendly tone → friendlier. Words
    are everywhere in a UI and matter at least as much as color or typeface.
- **Deciding:** if you lack a gut feeling, look at other sites your target audience uses and match
  their register (serious business vs playful). Do not borrow too much from direct competitors or
  you look like a second-rate copy.

### Limit your choices (ch. 1)
- **Definition:** Replace unlimited options with small, predefined sets of values (systems).
- **Why:** Unconstrained decisions are torture because several options are all "right" (12px vs
  13px, 10% vs 15% shadow opacity, 24px vs 25px avatar, medium vs semibold, 18px vs 20px margin).
  Buttons with near-identical backgrounds cannot be told apart by eye.
- **Define systems in advance:** e.g. 8–10 predefined shades of a color instead of the color
  picker; a restrictive type scale instead of 1px nudges. Hard work of picking values happens once.
- **Design by process of elimination:** with a sizing scale of 12/16/24/32px, guess (16px), compare
  the neighbors (12 and 24). If both outer options are obviously worse, the middle wins. If an
  outer option looks best, repeat using it as the new middle.
- **Systematize everything:** font size, font weight, line height, color, margin, padding, width,
  height, box shadows, border radius, border width, opacity — anything you catch yourself laboring
  over. You need not define all up front; adopt a system mindset and avoid making the same minor
  decision twice.

---

## Ch. 2 — Hierarchy is everything

### Visual hierarchy (ch. 2, "Not all elements are equal")
- **Definition:** How important the elements in an interface *appear* relative to one another.
- **Why:** It is the most effective tool for making something feel "designed"; it has nothing to
  do with artistic talent or superficial styling. When everything competes for attention the UI
  feels noisy and chaotic.
- **Apply:** Deliberately de-emphasize secondary and tertiary information and highlight the most
  important elements. The authors' example improves markedly with color scheme, font and layout
  unchanged.

### Size isn't everything (ch. 2)
- **Definition:** Do not control hierarchy with font size alone; use weight and color.
- **Why:** Size-only hierarchy yields primary content that is too large and secondary content too
  small to read.
- **Apply:** Make primary text bolder so it can use a more reasonable size; give supporting text
  a softer color instead of a tiny size.
- **Numbers:** two or three text colors (dark for primary, grey for secondary, lighter grey for
  tertiary); two font weights (normal = 400 or 500 depending on font; heavier = 600 or 700).
- **Pitfall:** Weights under 400 for UI text — fine for large headings, too hard to read small. To
  de-emphasize, use lighter color or smaller size, not a thinner weight.

### Don't use grey text on colored backgrounds (ch. 2)
- **Definition:** Grey works for de-emphasis on white because it *reduces contrast*; on a colored
  background grey does not reduce contrast in the same way and looks bad.
- **Why:** What creates hierarchy is moving the text color closer to the background color.
- **Apply:** Hand-pick a color with the same hue as the background and adjust saturation and
  lightness until it reads as secondary.
- **Pitfall:** White text with reduced opacity — looks dull, washed out, even disabled, and lets
  an image or pattern background show through the letters.

### Emphasize by de-emphasizing (ch. 2)
- **Definition:** When the main element cannot be made to stand out further, tone down its
  competitors instead.
- **Examples:** an active nav item that doesn't pop even with a different color → give inactive
  items a softer color. A sidebar competing with main content → remove the sidebar background so
  content sits directly on the page background.

### Labels are a last resort (ch. 2)
- **Definition:** Displaying data as `label: value` gives every piece equal emphasis and blocks
  hierarchy (this is about displaying data, not form accessibility).
- **Apply, in order:**
  1. No label when the format says what it is (`janedoe@example.com`, `(555) 765-4321`, `$19.99`)
     or context does ("Customer Support" under a name in a directory).
  2. Combine label and value: "In stock: 12" → "12 left in stock"; "Bedrooms: 3" → "3 bedrooms".
  3. Label as secondary content when scannability needs it (dashboards): smaller, lower
     contrast, lighter weight, or a combination.
  4. Emphasize the label when users scan *for* the label (spec sheets: they look for "depth",
     not "7.6mm"): darker label, slightly lighter value — don't de-emphasize data too much.

### Separate visual hierarchy from document hierarchy (ch. 2)
- **Definition:** Semantic element choice (h1/h2/h3) must not dictate visual size.
- **Why:** Browser defaults make h1 huge; in application UIs section titles behave like labels —
  supportive content that should not steal attention from the section's content.
- **Apply:** Titles like "Manage Account" can be an h1 and still be small. Sometimes keep the
  heading in markup for accessibility but hide it visually. Choose elements for semantics, style
  for hierarchy.

### Balance weight and contrast (ch. 2)
- **Definition:** Emphasis is driven by surface area (bold text covers more pixels). Weight and
  contrast counterbalance each other.
- **Contrast compensates for weight:** icons (especially solid ones) are heavy and feel
  emphasized next to text; you cannot thin an icon, so soften its color (lower contrast).
- **Weight compensates for contrast:** a 1px border in a soft color is too subtle, but darkening
  it feels harsh; increase its width instead to keep the soft color.

### Semantics are secondary (ch. 2)
- **Definition:** Design actions by their place in the hierarchy, not purely by semantics.
- **The pyramid:** most pages have one true primary action, a couple of secondary, a few
  seldom-used tertiary actions.
  - Primary: obvious — solid, high-contrast background.
  - Secondary: clear but not prominent — outline style or lower-contrast background.
  - Tertiary: discoverable but unobtrusive — styled like links.
- **Destructive actions:** destructive/high-severity does not automatically mean big, red, bold.
  If it is not the page's primary action, use secondary or tertiary styling, and reserve the big
  red treatment for the confirmation step where the destructive action *is* primary.

---

## Ch. 3 — Layout and spacing

### Start with too much white space (ch. 3)
- **Definition:** Give elements more room than feels necessary, then remove space until it looks
  right.
- **Why:** The usual approach adds space only until things stop looking actively bad, which is the
  minimum. "A little too much" on one element reads as "just enough" in a complete UI. Removing
  excess space is far easier to notice than needing to add it.
- **Exception:** dense UIs (dashboards showing a lot at once) are legitimate — but as a deliberate
  decision, never the default.

### Establish a spacing and sizing system (ch. 3)
- **Definition:** A constrained set of spacing/sizing values defined in advance.
- **Why a linear scale fails:** "multiples of 4px" does not help choose 120 vs 125. What matters
  is the *relative* difference between adjacent values: 12→16px is +33% and very visible; 500→520px
  is +4%, eight times less significant.
- **Rule:** no two adjacent values closer than about 25%.
- **Building it:** start with 16px (divides nicely; default browser font size); use factors and
  multiples; values are packed at the small end and spread progressively further apart going up.
  (See scales-and-systems.md for the scale.)
- **Using it:** when a gap is "not quite enough", the next value is probably perfect. Easier in the
  browser (typing numbers) than dragging. Produces subtle consistency.

### You don't have to fill the whole screen (ch. 3)
- **Definition:** Use only the width an interface needs; extra space at the edges never hurts.
- **Why:** Spreading things out or making them unnecessarily wide makes a UI harder to interpret.
  Needing 600px means use 600px, even on a 1200–1400px canvas. Sections need not be full width
  just because the nav is — don't worsen one element to match another.
- **Shrink the canvas:** if a small UI is hard to design on a large canvas, design on ~400px,
  mobile first; then adapt on larger screens (less changes than you expect).
- **Think in columns:** if a narrow element feels unbalanced in a wide UI, split it into columns
  (e.g. move a form's supporting text into a side column) rather than widening the form.
- **Don't force it:** equally, don't cram things into a small area when you do need space.

### Grids are overrated (ch. 3)
- **Definition:** A grid is just a constrained set of fluid percentage widths (12 columns = 8.33%
  each). Outsourcing every layout decision to it does harm.
- **Not all elements should be fluid:** a 3-column (25%) sidebar grows uselessly on wide screens
  and shrinks below its minimum on narrow ones (awkward wrapping/truncation). Give the sidebar a
  fixed width optimized for its contents; let the main area flex and use its own internal grid.
  Inside components too: use percentages only when you actually want scaling.
- **Don't shrink an element until you need to:** a login card at 6 columns (50%) on large and 8
  columns on medium creates a range where it is wider on medium than large. If 500px is optimal,
  set `max-width: 500px` and shrink only when the screen is narrower than that.

### Relative sizing doesn't scale (ch. 3)
- **Definition:** Ratios between elements are not constant across screen sizes or component sizes.
- **Example:** body 18px / headline 45px (2.5em) on desktop; body 14px on small screens makes the
  headline 35px, far too big; 20–24px (1.5–1.7×) is right. The relationship changed, so there was
  no real relationship worth encoding.
- **Rule:** large elements must shrink faster than small ones; the gap between small and large
  elements should be less extreme on small screens.
- **Within a component:** a button with 16px font, 16px horizontal padding, 12px vertical padding
  should not have padding defined in font-size terms. Larger buttons want disproportionately
  generous padding, smaller buttons disproportionately tighter padding — otherwise sizes feel like
  zoom, not like real size variants. Fine-tune properties independently.

### Avoid ambiguous spacing (ch. 3)
- **Definition:** When groups are not separated by borders or backgrounds, spacing alone must say
  which elements belong together.
- **Rule:** always more space *around* a group than *within* it.
- **Failures:** label-to-input gap equal to input-to-next-label gap (user may type into the wrong
  field); too little space above section headings; bullet gaps equal to a bullet's line height;
  same issue in horizontal layouts.

---

## Ch. 4 — Designing text

### Establish a type scale (ch. 4)
- **Why:** Without a system every pixel value from 10 to 24px ends up used; inconsistent and slow.
- **Modular scales** (ratio-based: 4:5 major third, 2:3 perfect fifth, 1:1.618 golden ratio, from a
  16px base): mathematically pure but (1) produce fractional sizes (31.25, 39.063, 48.828px) that
  browsers round differently — round them yourself if used; (2) give too few sizes for UI work (a
  rounded 3:4 scale yields 12, 16, 21, 28 and you will want sizes between 12–16 and 16–21; a tighter
  8:9 ratio is just reverse-engineering the sizes you wanted anyway).
- **Hand-crafted scale** (recommended for interfaces): pick values by hand; no rounding issues;
  total control; aligns with the spacing scale. Constrained enough to speed decisions, not so tight
  you miss a size.
- **Avoid em units** for the scale: nested ems compound (1.25em = 20px, then .875em inside gives
  17.5px — not on the scale). Use px or rem.

### Use good fonts (ch. 4)
- Safest: a neutral sans-serif (Helvetica-like). If you distrust your taste, the system font stack:
  `-apple-system, Segoe UI, Roboto, Noto Sans, Ubuntu, Cantarell, Helvetica Neue` — users already
  see it daily.
- Ignore typefaces with fewer than five weights; well-crafted families tend to have many. On
  Google Fonts filter "number of styles" to 10+ (weights × italics) — removes ~85% of options,
  leaving under 50 sans-serifs.
- Optimize for legibility: headline faces have tighter letter-spacing and shorter x-height; faces
  for small sizes have wider spacing and taller x-height. Avoid condensed, short-x-height faces for
  main UI text.
- Trust the crowd: sort by popularity, especially for non-neutral choices (a serif with character).
- Steal from people who care: inspect favorite sites' typefaces. Intuition follows.

### Keep your line length in check (ch. 4)
- 45–75 characters per line; achieve with a width of 20–35em. Slightly over 75 can work but is
  risky. Keep paragraphs at this width even when the content area is wider for images or large
  components — mixed widths look more polished.

### Baseline, not center (ch. 4)
- When mixing font sizes on one line (large card title + small actions), align baselines, not
  vertical centers. Center alignment looks off, especially when the texts sit close together; the
  baseline is a reference the eye already perceives.

### Line-height is proportional (ch. 4)
- 1.5 is only a starting point. Line-height exists to help the eye find the next line after a wrap.
- Line length: narrow content ~1.5; wide content up to ~2.
- Font size: inverse relationship — small text needs taller line-height; large headlines can use
  line-height 1.

### Not every link needs a color (ch. 4)
- Links in body copy must stand out and look clickable. In UIs where almost everything is a link,
  that treatment is overbearing: use a heavier weight or darker color instead. Ancillary links
  off the main path can get underline/color only on hover — discoverable without competing.

### Align with readability in mind (ch. 4)
- Align to the language direction (left for English). Center only headlines or short independent
  blocks; anything over two or three lines looks better left-aligned. If one centered block is too
  long, shorten the copy. Right-align numbers in tables so decimals line up. Justified text needs
  hyphenation enabled; it suits a print/magazine look, and left-aligned is fine there too.

### Use letter-spacing effectively (ch. 4)
- Default: trust the typeface designer. Two exceptions: tighten letter-spacing when using a
  legible-at-small-sizes family (Open Sans) for headlines to mimic a headline family (Oswald) —
  never the reverse, headline faces fail at small sizes even with added spacing; increase
  letter-spacing for all-caps text because uniform-height capitals have fewer distinguishing
  features than lowercase ascenders/descenders.

---

## Ch. 5 — Working with color

### Ditch hex for HSL (ch. 5)
- Hex/RGB hide visual similarity between colors in code; HSL exposes what the eye perceives.
- Hue: position on the wheel in degrees (0° red, 120° green, 240° blue). Saturation: 0% grey to
  100% vivid; at 0% hue is irrelevant. Lightness: 0% black, 100% white, 50% the pure hue.
- HSL ≠ HSB: in HSB 100% brightness is white only at 0% saturation; 100% saturation + 100%
  brightness in HSB equals 100% saturation + 50% lightness in HSL. Design tools favor HSB; browsers
  understand only HSL, so use HSL for the web.

### You need more colors than you think (ch. 5)
- Five-color palette generators are useless for real products. Three categories:
  - Greys: nearly everything (text, backgrounds, panels, form controls). 8–10 shades. Avoid true
    black (unnatural): start from a really dark grey and step to white in steady increments.
  - Primary: one, maybe two colors for primary actions and active nav; 5–10 shades. Ultra-light
    shades tint alert backgrounds; dark shades work for text.
  - Accents: attention-grabbers for new features (yellow, pink, teal); semantic states (red
    destructive, yellow warning, green positive); categorical colors for graph lines, calendar
    events, tags. Multiple shades each, used sparingly.
- A complex UI may need as many as ten colors × 5–10 shades.

### Define your shades up front (ch. 5)
- Do not generate shades on the fly with lighten/darken functions (ends in 35 near-identical
  blues). Fix the set up front.
- Base color first: for primary/accent, the shade that works as a button background. No numeric
  rule such as "50% lightness"; trust your eyes.
- Edges: darkest shade (usually text) and lightest (background tint). An alert component is a good
  test bed because it uses both. Keep the base hue; adjust saturation and lightness.
- Fill gaps: at least 5 shades, closer to 10. Nine is ideal: 900 darkest, 500 base, 100 lightest;
  pick 700 and 300 as midpoints, then 800/600/400/200 the same way.
- Greys: base matters less; darkest = darkest text color, lightest = subtle off-white background.
- Not a science: tweak saturation or lightness after real use; but avoid adding new shades often
  or the system is meaningless.

### Don't let lightness kill your saturation (ch. 5)
- Near 0% or 100% lightness the same saturation looks weaker; raise saturation as lightness moves
  away from 50% so light/dark shades don't wash out (visible on large areas).
- Perceived brightness: hues differ in inherent brightness at equal HSL lightness (yellow reads
  lighter than blue). Minima at red/green/blue (0°, 120°, 240°); maxima at yellow/cyan/magenta
  (60°, 180°, 300°). Formula is computed from RGB components (see scales-and-systems.md).
- Change brightness by rotating hue: lighter → rotate toward the nearest 60°/180°/300°; darker →
  toward 0°/120°/240°. Keeps intensity instead of pushing toward white/black. Example: darkening
  yellow by rotating toward orange gives warm, rich darks instead of dull brown. Combine with
  lightness adjustments. Limit rotation to 20–30° or it becomes a different color.

### Greys don't have to be grey (ch. 5)
- True grey has 0% saturation; most "greys" in practice are saturated. Blue → cool, yellow/orange
  → warm (like warm-white vs cool-white bulbs). Raise saturation at the light and dark ends to keep
  temperature consistent. Amount is a taste decision.

### Accessible doesn't have to mean ugly (ch. 5)
- WCAG: normal text (under ~18px) ≥ 4.5:1; large text ≥ 3:1.
- White text on color needs a surprisingly dark background to reach 4.5:1, and dark backgrounds
  grab attention — a hierarchy problem for non-focal elements. Flip the contrast: dark colored
  text on a light tint of the same color.
- Colored text on colored backgrounds (secondary text in a dark panel): adjusting only
  saturation/lightness ends near white; rotate the hue toward a brighter hue (cyan, magenta,
  yellow) to gain contrast while staying colorful.

### Don't rely on color alone (ch. 5)
- Colorblind users can't read red-vs-green metric cards; add icons (direction arrows). For graph
  lines, differentiate by contrast (light vs dark) rather than hue only. Color should support what
  the design already says, never be the sole channel.

---

## Ch. 6 — Creating depth

### Emulate a light source (ch. 6)
- One rule: light comes from above. Raised surfaces have a lighter top edge and darker bottom
  edge (door panel); inset surfaces have a shadow at the top (the lip blocks light) and a lighter
  bottom edge (cabinet panel).
- Raised element (button): people look slightly downward, so reveal a little of the top edge and
  hide the bottom. Top edge slightly lighter via a top border or inset box-shadow with a slight
  positive vertical offset — hand-pick the lighter color; overlaying semi-transparent white sucks
  the saturation out. Then a small, dark box-shadow with a slight vertical offset below; blur only
  a couple of pixels, sharp like the shadow under a wall outlet or window frame.
- Inset element (well, text input, checkbox): lighter bottom lip via bottom border or inset shadow
  with a negative vertical offset; small dark inset shadow with a slight positive vertical offset
  at the top so it does not poke through at the bottom.
- Don't get carried away: borrow cues, don't chase photo-realism — it makes UIs busy.

### Use shadows to convey elevation (ch. 6)
- Small, tight-blur shadows = slightly raised; large, high-blur = closer to the user. Closer
  attracts more focus. Buttons → small; dropdowns → medium; modals → large.
- Elevation system: a fixed set, five options is usually plenty; define smallest and largest,
  fill in between increasing roughly linearly.
- Interaction: add a shadow to a dragged item on click (pops forward); shrink or remove a button's
  shadow on press. Decide where an element sits on the z-axis, then assign the shadow.

### Shadows can have two parts (ch. 6)
- Shadow 1: larger, softer, considerable vertical offset, large blur — the cast shadow from a
  direct light source. Shadow 2: tighter, darker, smaller offset and blur — the area under the
  object where even ambient light barely reaches. Together: the big shadow stays subtle while the
  edges stay defined.
- Elevation: the tight ambient shadow fades as an object rises; keep it distinct at the lowest
  elevation and nearly or completely invisible at the highest.

### Even flat designs can have depth (ch. 6)
- Depth with color: lighter feels closer, darker further (especially within one color's shades).
  Lighter than background → raised; darker → inset.
- Solid shadows: short vertical offset, zero blur — stand-off without losing the flat look.

### Overlap elements to create layers (ch. 6)
- Offset a card across the boundary of two backgrounds; make an element taller than its parent
  so it overlaps both edges; overlap small controls (carousel). For overlapping images, add an
  "invisible border" in the background color so they never clash.

---

## Ch. 7 — Working with images

### Use good photos (ch. 7)
- Bad photos ruin otherwise good designs. Hire a professional (lighting, composition and color
  take years) or use high-quality stock (Unsplash is free). Never design around placeholders
  planning to swap in smartphone photos later — it never works.

### Text needs consistent contrast (ch. 7)
- The problem is the image's dynamics (light and dark areas), not the text color. Reduce the
  dynamics:
  - Semi-transparent overlay: black for light text, white for dark text (affects the whole image).
  - Lower the image contrast; compensate brightness.
  - Colorize: lower contrast → desaturate → solid fill with "multiply" blend. Also ties the image
    to brand colors.
  - Text shadow as a glow: large blur, no offset; still reduce image contrast, just less.

### Everything has an intended size (ch. 7)
- Never upscale bitmaps. Don't scale 16–24px icons to 3–4×: vector or not, they lack detail and
  feel chunky; enclose a near-native-size icon in a colored shape instead. Don't shrink
  screenshots (a 70% shrink turns 16px text into 4px): screenshot at a smaller layout (tablet),
  show a partial screenshot, or draw a simplified UI with lines for text. Don't downscale large
  icons either: a 128px logo at 16px favicon size turns to mush; redraw a simplified version at the
  target size.

### Beware user-uploaded content (ch. 7)
- Control shape and size: center images in fixed containers and crop (`background-size: cover`).
- Prevent background bleed (image background similar to UI background): subtle inner box-shadow,
  not a border (borders clash with image colors); or a semi-transparent inner border.

---

## Ch. 8 — Finishing touches

### Supercharge the defaults (ch. 8)
- Replace bullets with icons (checkmarks, arrows, or content-specific like a padlock). Promote
  testimonial quote marks into large colored visual elements. Style links: color/weight, or a
  thick colored underline that partially overlaps the text. Custom checkboxes/radios in a brand
  color for selected states.

### Add color with accent borders (ch. 8)
- A colored rectangle needs no graphic talent: top of a card, active nav item, side of an alert,
  short line under a headline, strip across the top of the whole layout.

### Decorate your backgrounds (ch. 8)
- Change the background color of a panel or section; subtle gradient with two hues no more than
  about 30° apart; subtle repeating pattern (Hero Patterns), full or along one edge; a simple
  geometric shape, a chunk of pattern, or a simplified world map. Keep contrast with the
  background low so content stays readable.

### Don't overlook empty states (ch. 8)
- For user-generated content, the empty state is the first impression — a priority, not an
  afterthought. Use an image/illustration and an emphasized call-to-action; hide tabs, filters and
  other supporting UI until there is content to act on.

### Use fewer borders (ch. 8)
- Borders are not the only separator and too many feel busy. Alternatives: box-shadow (best when
  the element's color differs from the background); two different background colors (and drop the
  border if you already have both); extra spacing.

### Think outside the box (ch. 8)
- Components need not match preconceptions: dropdowns can have sections, columns, supporting
  text, icons; tables can merge related non-sortable columns with internal hierarchy, add images
  and color; important radio groups can be selectable cards.

---

## Ch. 9 — Leveling up

- Look for decisions you wouldn't have made: whenever a design impresses you, ask what the
  designer did that you would never have thought of (inverted datepicker background, a button
  inside a text input, two font colors in one headline).
- Rebuild favorite interfaces from scratch without inspecting dev tools; diagnosing the
  differences teaches tricks like reduced heading line-height, letter-spacing on uppercase, and
  combining multiple shadows.

---

## Glossary of the authors' terms

| Term | Meaning (as used in the book) |
|---|---|
| Visual hierarchy | How important elements appear relative to each other (ch. 2) |
| Document hierarchy | Semantic structure (h1–h6) — independent of visual size (ch. 2) |
| Primary / secondary / tertiary (content or actions) | Levels of importance; each gets a distinct treatment (ch. 2) |
| Emphasize by de-emphasizing | Make X stand out by toning down its competitors (ch. 2) |
| Weight vs contrast | Surface area vs color difference; each can counterbalance the other (ch. 2) |
| Spacing and sizing system | Predefined non-linear scale of px values, 16px base (ch. 3) |
| Ambiguous spacing | Equal gaps inside and around a group, hiding grouping (ch. 3) |
| Modular scale / hand-crafted scale | Ratio-generated vs hand-picked type sizes (ch. 4) |
| HSL vs HSB | Hue/saturation/lightness (browser) vs brightness (design tools) (ch. 5) |
| Perceived brightness | Inherent brightness of a hue independent of HSL lightness (ch. 5) |
| Shades 100–900 | Nine-step naming: 900 darkest, 500 base, 100 lightest (ch. 5) |
| Color temperature | Cool (blue-saturated) vs warm (yellow/orange-saturated) greys (ch. 5) |
| Flipping the contrast | Dark colored text on light tint instead of white on dark color (ch. 5) |
| Elevation | Position on the virtual z-axis expressed by shadow size (ch. 6) |
| Two-part shadow | Soft cast shadow + tight ambient shadow (ch. 6) |
| Invisible border | Background-colored gap around overlapping images (ch. 6) |
| Intended size | The size a bitmap, icon or screenshot was drawn for (ch. 7) |
| Background bleed | Uploaded image's background merging with the UI background (ch. 7) |
| Accent border | A colored rectangle used as decoration (ch. 8) |
| Empty state | First screen of a feature before user content exists (ch. 8) |
