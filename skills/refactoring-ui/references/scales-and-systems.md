# Scales, numbers and systems — Refactoring UI

Every numeric value, threshold and ratio the authors give, in one place, for quick lookup when
writing CSS, tokens or a design-system config. Chapter cited for each.

Values marked **[image]** appear in the book only as a figure. They were read directly from the
PDF figures (pp. 63, 91, 92, 134, 161–162) and verified by the lead — safe to rely on.

## Table of contents

1. [Systems to define (master list)](#systems-to-define-master-list)
2. [Spacing and sizing scale](#spacing-and-sizing-scale)
3. [Type scale](#type-scale)
4. [Font weights and text colors](#font-weights-and-text-colors)
5. [Line length, line-height, alignment, letter-spacing](#line-length-line-height-alignment-letter-spacing)
6. [Font selection filters](#font-selection-filters)
7. [Color: HSL reference](#color-hsl-reference)
8. [Color palette sizes](#color-palette-sizes)
9. [Shade scale (100–900) construction](#shade-scale-100900-construction)
10. [Hue rotation and perceived brightness](#hue-rotation-and-perceived-brightness)
11. [Contrast / accessibility thresholds](#contrast--accessibility-thresholds)
12. [Shadow / elevation system](#shadow--elevation-system)
13. [Depth recipes (light-source numbers)](#depth-recipes-light-source-numbers)
14. [Layout numbers](#layout-numbers)
15. [Image numbers](#image-numbers)
16. [Finishing-touch numbers](#finishing-touch-numbers)
17. [Button hierarchy table](#button-hierarchy-table)
18. [Personality factor table](#personality-factor-table)

---

## Systems to define (master list)

The authors recommend a predefined set of values for (ch. 1 "Limit your choices"):
font size · font weight · line height · color · margin · padding · width · height · box shadows ·
border radius · border width · opacity · "anything else where you labor over a low-level decision".
You do not need all of them on day one; add a system each time you catch yourself making the same
minor decision twice.

**Choosing within a system — process of elimination (ch. 1):** guess a value, compare it with its
two neighbors on the scale; if both neighbors are clearly worse, keep the middle; if a neighbor is
better, make it the new middle and compare again. Works for any system where adjacent values look
noticeably different.

---

## Spacing and sizing scale

Rules (ch. 3):
- Linear scales (e.g. "every multiple of 4px") do not work because relative difference matters:
  12→16px = +33% (large), 500→520px = +4% (imperceptible, 8× less significant).
- No two adjacent values closer than ~25%.
- Base value 16px (divides nicely; default browser font size). Build from factors and multiples.
- Small end packed tightly, large end spread out.

Example scale from the book **[image, verified p. 63]** — every value is 16 × a factor
(0.25, 0.5, 0.75, 1, 1.5, 2, 3, 4, 6, 8, 12, 16, 24, 32, 40, 48):

```
4  8  12  16  24  32  48  64  96  128  192  256  384  512  640  768
```

Relative steps: 4→8 +100%, 8→12 +50%, 12→16 +33%, 16→24 +50%, 24→32 +33%, 32→48 +50%, 48→64 +33%,
64→96 +50%, 96→128 +33%, then +50%/+33% alternating up to 768. Every step ≥ 25%.

Usage rule (ch. 3): need a bit more space? Take the *next* value on the scale rather than nudging
by pixels. Use the same scale for widths, heights, paddings, margins and icon sizes.

---

## Type scale

Rules (ch. 4):
- Don't use a linear scale. Don't let every value 10–24px creep into the UI.
- Modular scale caveats: ratios 4:5 (major third), 2:3 (perfect fifth), 1:1.618 (golden ratio)
  from a 16px base. Produces fractional sizes (31.25, 39.063, 48.828px) — round them yourself to
  avoid off-by-one rendering differences between browsers. A rounded 3:4 scale gives
  12/16/21/28px, which lacks the in-between sizes UI work needs.
- Hand-crafted scale preferred for UI; aligns with the spacing scale.
- Define in **px or rem**, never em (nesting compounds: 1.25em → 20px context, then .875em →
  17.5px, which is off-scale). The book's em-scale counter-example (p. 92): `.75em .875em 1em 1.25em 1.5em`.

Hand-crafted scale from the book **[image, verified p. 91]** (px):

```
12  14  16  18  20  24  30  36  48  60  72
```

Responsive note (ch. 3 "Relative sizing doesn't scale"): large text shrinks faster than small
text. Example: 18px body / 45px headline (2.5×) on desktop; on mobile with 14px body, headline
should be 20–24px (1.5–1.7×), not 35px.

---

## Font weights and text colors

| Role | Value (ch. 2) |
|---|---|
| Normal weight for most UI text | 400 or 500 (depends on the typeface) |
| Emphasis weight | 600 or 700 |
| Weights below 400 | Avoid for UI text; acceptable only for large headings |
| Number of weights in use | Two is usually enough |
| Text color roles | 2–3: dark (primary), grey (secondary), lighter grey (tertiary) |

De-emphasis order of preference (ch. 2): lighter color, smaller size — not a thinner weight. On
colored backgrounds: same hue as background, adjusted saturation/lightness — not grey, not white at
reduced opacity.

---

## Line length, line-height, alignment, letter-spacing

| Property | Rule | Source |
|---|---|---|
| Line length | 45–75 characters per line; width 20–35em. >75 is risky. | ch. 4 |
| Paragraph width in wide content areas | Keep paragraphs at the above width even if images/components are wider | ch. 4 |
| Line-height baseline | ~1.5 as a starting point only | ch. 4 |
| Line-height vs line length | Narrow content ~1.5; wide content up to 2 | ch. 4 |
| Line-height vs font size | Inverse: small text taller; large headlines down to 1 | ch. 4 |
| Mixed font sizes on one line | Align by baseline, not vertical center | ch. 4 |
| Centered text | Only headlines / blocks of ≤ 2–3 lines; longer → left-align or shorten the copy | ch. 4 |
| Numbers in tables | Right-align (decimal alignment) | ch. 4 |
| Justified text | Enable hyphenation; print/magazine look only | ch. 4 |
| Letter-spacing default | Leave as designed | ch. 4 |
| Headlines in a small-size-optimized family | Decrease letter-spacing (never the reverse) | ch. 4 |
| All-caps text | Increase letter-spacing | ch. 4 |
| Links in link-dense UIs | Heavier weight or darker color instead of link color; ancillary links underline/color on hover only | ch. 4 |

---

## Font selection filters

(ch. 4 "Use good fonts")
- Default safe choice: neutral sans-serif (Helvetica-like).
- System stack: `-apple-system, Segoe UI, Roboto, Noto Sans, Ubuntu, Cantarell, Helvetica Neue`.
- Reject families with fewer than 5 weights. On Google Fonts, filter "number of styles" ≥ 10
  (weights + italics): eliminates ~85% of options, leaving < 50 sans-serifs.
- For UI body text avoid condensed faces with short x-height (those are headline faces: tight
  spacing, short lowercase). Faces for small sizes have wider spacing and taller x-height.
- Sort by popularity; inspect typefaces on sites you admire.

---

## Color: HSL reference

(ch. 5 "Ditch hex for HSL")

| Component | Range / anchors |
|---|---|
| Hue | degrees on the wheel: 0° red, 120° green, 240° blue |
| Saturation | 0% grey (hue irrelevant) → 100% vivid |
| Lightness | 0% black, 50% pure hue, 100% white |

HSB differs: 100% brightness is white only at 0% saturation; HSB (S 100%, B 100%) = HSL (S 100%,
L 50%). Browsers understand HSL, not HSB.

---

## Color palette sizes

(ch. 5 "You need more colors than you think")

| Category | How many colors | Shades each | Uses |
|---|---|---|---|
| Greys | 1 scale | 8–10 | text, backgrounds, panels, form controls — most of the UI |
| Primary | 1, maybe 2 | 5–10 | primary actions, active nav; ultra-light = alert tint, dark = text |
| Accents | several | multiple (5–10) | attention (yellow/pink/teal), semantic red/yellow/green, categorical (graph lines, calendar events, tags) |

Total for a complex UI: up to ~10 colors × 5–10 shades. Five hex codes from a generator are not a
usable palette. Avoid true black for greys — start from a very dark grey.

---

## Shade scale (100–900) construction

(ch. 5 "Define your shades up front")
1. Pick the **base (500)**: for primary/accent colors, the shade that works as a button
   background. No fixed lightness rule; judge by eye.
2. Pick the **darkest (900)**: typically used for text. Pick the **lightest (100)**: typically a
   tinted background. Keep the base hue; adjust saturation and lightness. Prototype them in an
   alert component (uses both).
3. Fill **700 and 300** as perceptual midpoints between their neighbors.
4. Fill **800, 600, 400, 200** the same way.
5. Minimum 5 shades per color; closer to 10 for comfort; 9 divides nicely.
6. Greys: base matters less. 900 = darkest text color; 100 = subtle off-white background. Fill
   from the edges inward.
7. After real use, tweak individual shades by eye; resist adding new shades.
8. Never compute shades with lighten()/darken() at use sites.

Saturation correction (ch. 5 "Don't let lightness kill your saturation"): increase saturation as
lightness moves away from 50% (both toward 100% and toward 0%) so the ends don't look washed out.
Same for tinted greys (ch. 5 "Greys don't have to be grey"): raise saturation on the lightest and
darkest greys to keep a consistent cool (blue) or warm (yellow/orange) temperature.

---

## Hue rotation and perceived brightness

(ch. 5)
- Perceived brightness formula as printed in the book **[image, verified p. 134]**:
  `sqrt(0.299·r² + 0.587·g² + 0.114·b²) / 255` (r, g, b = 0–255). Example: yellow (H60 S100% L50%)
  and blue (H240 S100% L50%) share the same HSL lightness, yet yellow is perceived far lighter.
- Around the wheel at S 100% / L 50%: local minima (darkest) at red 0°, green 120°, blue 240°;
  local maxima (brightest) at yellow 60°, cyan 180°, magenta 300°.
- To **lighten** without washing out: rotate hue toward the nearest of 60°, 180°, 300°.
- To **darken** without muddying: rotate toward the nearest of 0°, 120°, 240°.
- Combine with lightness changes. Maximum rotation **20–30°**; more reads as a different color.
- Example: a yellow palette gets warm, rich dark shades by rotating toward orange as lightness
  decreases.
- Accessibility use (ch. 5): colored secondary text on a dark colored panel — rotate toward a
  brighter hue (cyan/magenta/yellow) to raise contrast instead of going near-white.

---

## Contrast / accessibility thresholds

(ch. 5 "Accessible doesn't have to mean ugly", "Don't rely on color alone")

| Case | Threshold / rule |
|---|---|
| Normal text (under ~18px) | contrast ratio ≥ 4.5:1 (WCAG) |
| Large text | ≥ 3:1 |
| White text on colored bg | needs a dark color; if that over-emphasizes a non-focal element, flip to dark colored text on a light tint |
| Information encoded in color | must also be encoded another way (icons, labels) |
| Multi-series graphs | vary lightness/contrast between series, not just hue |

---

## Shadow / elevation system

(ch. 6)
- Fixed set of shadows; **five** is usually plenty. Define the smallest and largest, fill the
  middle so sizes grow roughly linearly. The book's five **[image, verified p. 161]**:

  ```
  0 1px  3px  hsla(0,0%,0%,.2)   /* 1 – barely raised: buttons, cards */
  0 4px  6px  hsla(0,0%,0%,.2)   /* 2 */
  0 5px  15px hsla(0,0%,0%,.2)   /* 3 – dropdowns, popovers */
  0 10px 24px hsla(0,0%,0%,.2)   /* 4 */
  0 15px 35px hsla(0,0%,0%,.2)   /* 5 – modals, highest attention */
  ```
  Interaction example (p. 162): button at rest `0 4px 6px hsla(0,0%,0%,.2)`, on click
  `0 1px 3px hsla(0,0%,0%,.2)` (sinks into the page).
- Mapping: small/tight blur → barely raised (buttons); medium → dropdowns; large/wide blur → modals
  (highest attention).
- Two-part shadow (ch. 6):

| Part | Offset | Blur | Darkness | Role | Over elevation |
|---|---|---|---|---|---|
| Cast shadow | considerable vertical | large | lighter/subtle | direct light | grows with elevation |
| Ambient shadow | small vertical | small | darker | light blocked under the edges | fades: distinct at lowest, almost/completely invisible at highest |

- Interaction states: draggable item gains a shadow on press (lifts); pressed button loses or
  shrinks its shadow (sinks).
- Flat alternative: solid shadow with short vertical offset and 0 blur.

---

## Depth recipes (light-source numbers)

(ch. 6 "Emulate a light source")

| Goal | Edge treatment | Shadow |
|---|---|---|
| Raised (button) | top edge slightly lighter than face: top border or inset box-shadow with slight **positive** vertical offset; hand-picked color, not translucent white | small dark box-shadow, slight positive vertical offset, blur a couple of px, sharp edges |
| Inset (well, input, checkbox) | bottom edge slightly lighter: bottom border or inset shadow with **negative** vertical offset | small dark **inset** shadow with slight positive vertical offset at the top |
| Flat-design raised | element lighter than background | optional solid 0-blur shadow |
| Flat-design inset | element darker than background | — |

---

## Layout numbers

| Item | Value | Source |
|---|---|---|
| Historic desktop width | 960px; modern canvases 1200–1400px — don't fill them by default | ch. 3 |
| Mobile-first canvas | ~400px | ch. 3 |
| 12-column grid column | 8.33% | ch. 3 |
| Fixed vs fluid | sidebars and similar: fixed width tuned to content; main area flexes | ch. 3 |
| Max-width pattern | e.g. login card `max-width: 500px`; shrink only below that viewport width | ch. 3 |
| Button example | 16px font, 16px horizontal padding, 12px vertical padding; padding not font-relative | ch. 3 |
| Grouping | space around a group > space within it | ch. 3 |
| Narrow element in wide UI | split into columns (e.g. form + side column of helper text) instead of widening | ch. 3 |

---

## Image numbers

| Item | Value | Source |
|---|---|---|
| Icon intended size | icons drawn at 16–24px look chunky at 3–4×; wrap in a colored shape instead | ch. 7 |
| Screenshot shrink | 70% shrink → 16px text becomes ~4px; use tablet-size screenshot, partial crop, or simplified drawing | ch. 7 |
| Favicon | 128px logo → 16px turns to mush; redraw simplified at 16px | ch. 7 |
| Text-on-image fixes | black overlay (light text) / white overlay (dark text); lower image contrast + adjust brightness; colorize = lower contrast → desaturate → solid fill, multiply blend; text-shadow glow = large blur, 0 offset | ch. 7 |
| User uploads | fixed container, center + crop (`background-size: cover`); inner box-shadow or semi-transparent inner border against bleed, not a solid border | ch. 7 |

---

## Finishing-touch numbers

| Item | Value | Source |
|---|---|---|
| Background gradient | two hues ≤ ~30° apart | ch. 8 |
| Patterns / decorative shapes | low contrast against the background | ch. 8 |
| Accent border positions | card top, active nav, alert side, under headline, top of layout | ch. 8 |
| Separation without borders | box-shadow (element color ≠ background), different background colors, extra spacing | ch. 8 |

---

## Button hierarchy table

(ch. 2 "Semantics are secondary")

| Level | Count per page | Treatment |
|---|---|---|
| Primary | one | solid, high-contrast background |
| Secondary | a couple | outline, or low-contrast background |
| Tertiary | a few | link-styled |
| Destructive, not primary on this page | — | secondary/tertiary style; big red bold only on the confirmation step where it is primary |

---

## Personality factor table

(ch. 1 "Choose a personality")

| Factor | Option → feel |
|---|---|
| Typeface | serif → elegant/classic; rounded sans → playful; neutral sans → plain/neutral |
| Color | blue → safe, familiar; gold → expensive, sophisticated; pink → fun |
| Border radius | none → serious/formal; small → neutral; large → playful; never mix |
| Language | impersonal → official; casual → friendly |
