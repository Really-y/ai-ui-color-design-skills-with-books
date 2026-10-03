# Applying Albers' laws to interface and visual design

> **Scope note.** Everything in this file is *application derived from Albers' laws* by the
> extractor. Albers wrote about color paper, painting and teaching, not about screens, data
> visualization or brand systems. Each entry cites the law it rests on (chapter in parentheses) so
> the derivation can be checked; the derived advice itself is not Albers' own words. Where a
> recommendation adds something the book does not say (e.g. accessibility thresholds), it is marked
> "(extractor note)".

## Contents
1. Working method: how to evaluate any color decision
2. Palettes and design tokens
3. Backgrounds, surfaces and the influence of the ground
4. Text on color and figure/ground legibility
5. Data visualization
6. Brand colors and their reproduction
7. UI states, emphasis and hierarchy
8. Scales: greys, tints, shades, elevation
9. Space, layering and transparency
10. Quantity, placement and recurrence in layouts
11. Reviews and critique of visual work
12. Checklist

---

## 1. Working method: how to evaluate any color decision

- **Judge in context, never in isolation** — "we almost never see a single color unconnected and
  unrelated to other colors" (ch. II); a color "has many faces" (ch. IV). A swatch in a token file
  or a color picker is a *factual fact*; what appears on the rendered screen next to its neighbors
  is the *actual fact* (ch. XXV terms). Evaluate the rendered composition at real size, on the real
  background, with the real neighbors.
- **Compare side by side, under equal conditions** (ch. IV, V, XIV): same size, same ground, no gap
  between the swatches being compared. Comparing across a gap or across two separate mockups is
  "poor psychological engineering" (ch. XIV); overlay or swap patches instead.
- **Do not trust memory or names** (ch. I): "brand blue" in two people's heads is two blues. Always
  pull the sample.
- **Expect to be wrong about lightness** (ch. V: 60% wrong across hues). Verify every lightness
  claim with a test — the after-image test, a side-by-side contiguous mount, or a measured
  luminance (extractor note: measuring is Albers' "factual fact"; perceived order can still differ
  from it, so look as well as measure).
- **Treat screenshots, exports and prints as different instruments** (ch. V, XIX): they shift
  lightness and brightness. Check on the target device/medium.
- **Taste while cooking** (ch. XVI): no palette generator, harmony rule or token system can
  precalculate "changed and changing light", several light sources, reflections, reading order,
  materials and neighboring objects. Iterate on the real screen.

## 2. Palettes and design tokens

- **Harmony rules are not a design method.** Complementary, split-complementary, triad and tetrad
  pickers produce "pleasant, beautiful, and thus convincing" charts that are "presented in a most
  theoretical and least practicable manner" because every member appears in the same quantity,
  shape, count and often lightness (ch. XVI). A palette is only testable once each color has its
  real area and recurrence. Build mockups with realistic proportions before approving a palette.
- **Any colors can work together if their quantities are appropriate** (ch. XVI). When a stakeholder
  rejects a combination, first try changing quantities (areas, number of occurrences) and placement
  before changing the colors.
- **Design the cast, then the performances** (ch. XVI). Define a small set of colors and derive
  different "scenes" (marketing page, dense dashboard, dark mode, print) by redistributing quantity
  and dominance — not by adding colors. "With fewer means toward more action" (ch. XVIII).
- **Every color has two decisive characteristics**: light intensity (lightness) and color intensity
  (brightness) (ch. XIV). Specify both for each token and note which neighbors it is intended to sit
  next to.
- **Prefer "variants" to "variety"** (ch. XXV): when extending a palette, re-do a part thoroughly
  within the scheme rather than adding a new hue "for variety's sake."
- **Warm/cool labels are relative** (ch. XXI): a "warm grey" is warm only next to a cooler one. Do
  not let a token name promise a temperature that the context will contradict.
- **Dissonance is allowed** (ch. XVI, XXIV): a deliberately tense accent can be right; equilibrium
  of tensions is as valid as symmetric harmony.

## 3. Backgrounds, surfaces and the influence of the ground

- **The ground is the influencing color; the content is the influenced color** (ch. IV). Large
  backgrounds (page, card, sidebar) change every small element on them in light and in hue
  simultaneously. Decide backgrounds first, then test foreground tokens on each background.
- **Subtraction of color** (ch. VII): a ground subtracts its own hue and its own lightness from what
  it carries. A blue-tinted surface makes blue accents look greyer and less blue; a light surface
  eats the lightness of light elements; a dark surface swallows dark ones. The same accent token on
  a white card and on a tinted panel is *two* colors to the user.
- **Dark mode is not inversion**: the same hue on a dark ground is pushed lighter and its hue is
  pushed toward the complement of the ground (ch. IV, VIII). Re-tune accents per background instead
  of reusing one value.
- **The more different the grounds, the stronger the influence** (ch. VII). A component that must
  look identical on very different surfaces (white page, brand-colored hero, photo) needs
  per-surface variants or a neutral local ground (a card) that equalizes conditions.
- **Avoid influence from too many directions** (ch. IV): a small element surrounded by four
  different colored neighbors reads unpredictably — "lacks both sight and insight." Give important
  elements a single, calm surrounding.
- **Amount reduces distance** (ch. XVI): a large area of one color feels near and intimate; a
  large saturated background will dominate the whole screen's mood.

## 4. Text on color and figure/ground legibility

- **Legibility is a light-intensity question first** (ch. V, XXIII). Hue contrast alone does not
  separate figure from ground; two colors of equal light intensity make the boundary vanish (ch.
  XXIII), and contrasting hues at near-equal lightness make it vibrate (ch. XXII) — "aggressive",
  "uncomfortable", "disliked." Red text on green, blue on magenta, orange on mid-grey are classic
  cases. Test text/background pairs by lightness, not by hue wheel distance.
- **Vanishing boundaries are the rarest effect to achieve and the commonest accidental failure.**
  Disabled states, placeholder text, subtle borders and chart gridlines are where designers
  unknowingly produce "almost-equals" (ch. XXIII). Decide deliberately how far from equality each
  must be. (Extractor note: Albers gives no numeric threshold; accessibility ratios such as WCAG are
  one factual measure, but still verify by eye in context.)
- **Soft boundary = connected; hard boundary = separated** (ch. XI). Body text wants a hard boundary
  with its ground; a decorative tint wants a soft one. If text looks "fuzzy", the boundary is too
  soft — raise the light-intensity difference before touching hue.
- **Thin figures are the most influenced** (ch. IV: small amounts on large grounds change most).
  Small type, hairlines and icons on colored grounds shift visibly; thicker weights resist
  influence better.
- **Reading context** (ch. II): all-caps and undifferentiated letterforms read worst; Albers judged
  sans-serif body text "uneasy." Whatever the typeface, the lesson is that legibility comes from
  differentiation and context, not from simplicity alone.
- **Photographs and reproductions will not tell you if text is legible** on colored grounds (ch.
  V); look at the live rendering.

## 5. Data visualization

- **Categorical palettes must survive subtraction and influence** (ch. IV, VII). A series color that
  is distinguishable in the legend (on white) may be absorbed when plotted on a tinted plot area or
  next to a neighboring series. Test series colors in the chart, adjacent to each other, at the
  thickness they will have (thin lines are strongly influenced).
- **Sequential scales obey Weber-Fechner** (ch. XX). Equal numeric steps in opacity or layered tint
  do not read as equal; a visually even ramp needs geometric (logarithmic) physical steps. Verify
  a ramp as contiguous swatches: boundaries should look equally distinct along the whole scale;
  boundaries that soften toward one end mean the steps are compressing (ch. XX).
- **Gradation studies' rule** (ch. V): never separate scale steps with lines or gaps when you need
  to judge them; compare contiguous.
- **Legends are harmony charts** (ch. XVI): equal little squares in equal quantity. The chart itself
  shows the colors in very different quantities; judge the chart, not the legend.
- **Optical mixture** (ch. XII): small dots, thin hatching and dense scatter merge into a new color
  at distance; the effect "depends on size and on distance." A scatter of red and blue points reads
  as violet from across the room. Pick mark sizes with the viewing distance in mind.
- **Bezold effect** (ch. XIII): changing one recurring element (gridlines, outlines, background
  weave) can re-tint the whole visualization. Use it deliberately (change the gridline color to shift
  the mood) and watch for it accidentally.
- **Fluting / intersecting colors** (ch. XV): in a stacked band of related tints, each band appears
  lighter at the edge next to its darker neighbor and darker next to its lighter one. Heatmaps and
  choropleths show false gradients inside flat cells for this reason.
- **Middle mixtures look frontal and flat** (ch. XI): a mid tone equidistant from its neighbors
  will not sort itself spatially; use boundary hardness, not hue, to push layers apart.
- **Film-color softness** (ch. XIV): very small lightness steps between neighboring layers produce
  a translucent, filmy look; use it for backgrounds, avoid it where categories must separate.

## 6. Brand colors and their reproduction

- **A brand color is a factual fact; its appearance is an actual fact** (ch. XXV). It will look
  different on every ground, material, lighting and medium — "changed, lost, and reversed" (ch.
  XVI). Specify the brand color *with* its intended grounds and neighbors, not as a lone value.
- **Reproduction changes instrumentation** (ch. XIX, V): screens (direct light, additive — mixtures
  gain light) and print (reflected, subtractive — mixtures lose light) behave oppositely (ch. X);
  halftone printing turns opaque colors into transparent optical mixtures over white; color
  photography overemphasizes blue and red and greens the whites (ch. V). Proof brand colors per
  medium and expect to adjust values rather than demand one number everywhere.
- **Color memory and naming are unreliable** (ch. I): "Coca-Cola red" is remembered as many reds.
  Brand consistency comes from controlled context, not from users recalling a value.
- **Fine effects do not survive photomechanical processes** (Preface, ch. XXIII): equal-lightness
  pairings, delicate tints and near-equal boundaries are the first to be destroyed in reproduction.
  Build brand systems on robust differences.

## 7. UI states, emphasis and hierarchy

- **Emphasis is quantity and pronouncement** (Intro, ch. XVI): "quantity is a quality" — amount and
  recurrence establish "weight in space — and weight in time." The primary action should hold the
  dominant quantity *or* the hardest boundary; secondary elements get softer boundaries and smaller
  amounts. Do not try to make everything "equally important."
- **One cast, several performances** (ch. XVI): default, hover, active, disabled, selected can be
  the same small set redistributed in quantity and placement; a disabled state is a state of lower
  pronouncement (softer boundary, less amount), not a new hue.
- **Separation needs hard boundaries used sparingly** (Cézanne, ch. XI): emphasize borders only
  where a layer must separate (modal over page, focus ring); elsewhere let areas connect with soft
  boundaries so the surface does not look "flat and frontal" everywhere.
- **Color changes with its neighbors, so states change with context** (ch. IV): the same "active"
  tint reads differently inside a dark navigation rail and on a white content area. Test each state
  in each container.
- **Vibrating boundaries are not energy** (ch. XXII): a saturated accent on a saturated ground of
  equal lightness feels aggressive; reserve it, if ever, for deliberate alarm.

## 8. Scales: greys, tints, shades, elevation

- **Collect many steps, then choose**; commercial/preset scales offer "too limited choice, or,
  worse, unequal steps" (ch. V). Generate more candidates than you need and select by eye.
- **Steps must look equal, not measure equal** (ch. XX): build with geometric physical increments
  and verify contiguously; "the softer the steps appear, and the more equal the steps are, the more
  valuable" (ch. V).
- **Relativity deflects scales in use** (ch. XX): a step that is even in the scale is uneven once a
  step sits on a different ground; re-check elevation/surface tints in situ.
- **Keep swatch proportions wide** (ch. XX): narrow deep steps do not stay visually level; broad
  steps may flute.

## 9. Space, layering and transparency

- **Depth is read from boundaries** (ch. XI): "softer boundaries disclose nearness implying
  connection, harder boundaries indicate distance, separation." Layer order in a UI is communicated
  by boundary hardness as much as by shadows.
- **Fake transparency is a mixture choice** (ch. IX, XI): an overlap reads as transparent when the
  overlap color is a believable mixture of the two parents — neither lighter than the lighter nor
  darker than the darker, not more or less intense than either — and when the overlap area is
  generous. This lets you render "glass" and overlays with opaque tokens, predictably, instead of
  with alpha (whose result depends on whatever is underneath).
- **Dominance in the mixture decides which layer is in front** (ch. XI, Plate XI-3): if the overlap
  leans toward layer A, A reads in front; a true middle mixture reads as "optical penetration" —
  both on one plane.
- **Film color vs. surface color** (ch. XVII): tints, scrims and semi-transparent overlays are film
  colors — a layer between the eye and the object. Volume color (fluids) deepens with thickness, a
  natural model for stacked translucent layers getting darker (ch. XVII, XX).

## 10. Quantity, placement and recurrence in layouts

- Ask for every color: **how much** (area) and **how often** (recurrence) (ch. XVI). A color that
  recurs often carries "weight in time" even if each instance is small.
- Schopenhauer's quantities (yellow 3 : orange 4 : red 6 : violet 9 : blue 8 : green 6; ch. XVI)
  are a historical example of balancing lightness with area: lighter colors need less area to hold
  their own. Use the principle (balance by quantity), not the numbers.
- Equal quantities for all members "unify them, but at the expense of the more important inner
  relatedness" (ch. XVI). Decide which color dominates each screen.
- **Placement**: sideward (left–right) contact makes interaction easiest to read (ch. XVIII); a
  color between two others is read in relation to both and may split into two (ch. XV).
- Try 4 distributions of the same cast before choosing (ch. XVI).

## 11. Reviews and critique of visual work

See `teaching-and-critique.md`. Applied to design review:
- Put all candidates on the wall/screen at once; sort by promise; compare "forth and back."
- Name the single effect each screen must achieve; judge whether a viewer could misread it.
- Ask questions, show by comparison; admit "cannot decide" and test instead of asserting.
- Ask for variants (thorough re-doings within the scheme), not variety.
- Make reviewers work with the palette they dislike before they reject it (ch. V, XVIII).

## 12. Checklist

- [ ] Every color was judged on its real ground, with its real neighbors, at real size.
- [ ] Lightness order of text/background, series, states verified by test, not by assumption.
- [ ] No unintended near-equal lightness pairs (disabled text, borders, gridlines, badges).
- [ ] No unintended vibrating pairs (saturated hue contrast at equal lightness).
- [ ] Scales built with geometric steps and checked contiguously; boundaries equally distinct.
- [ ] Accents re-tuned per background (light, dark, tinted, image) — subtraction accounted for.
- [ ] Quantities and recurrence set so the intended color dominates; not all members equal.
- [ ] Layer order expressed by boundary hardness; overlaps use believable mixtures.
- [ ] Palette judged in a realistic mockup, not in a harmony chart or legend.
- [ ] Checked on the target medium/device; reproductions not used as proof.
- [ ] Variants compared side by side before the final choice.
