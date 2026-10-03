# UI audit checklist — Refactoring UI

Walk a screen (or a PR touching styling) top to bottom. Each line is a yes/no check derived from
the book; chapter in parentheses. Mark failures and route to playbook.md for the fix. The order
follows the authors' chapters so a review can be reported chapter by chapter.

## Table of contents

0. [Before you start](#0-before-you-start)
1. [Starting from scratch / process](#1-starting-from-scratch--process)
2. [Hierarchy](#2-hierarchy)
3. [Layout and spacing](#3-layout-and-spacing)
4. [Text](#4-text)
5. [Color](#5-color)
6. [Depth](#6-depth)
7. [Images](#7-images)
8. [Finishing touches](#8-finishing-touches)
9. [Systems and tokens (code-level review)](#9-systems-and-tokens-code-level-review)
10. [Reporting template](#10-reporting-template)

---

## 0. Before you start

- [ ] Identify the screen's single primary action and its primary content. Everything else is
      secondary or tertiary (ch. 2).
- [ ] Note the intended personality (serious vs playful) so judgments about radius, color and copy
      are consistent (ch. 1).
- [ ] If possible, view the screen in grayscale once; hierarchy should survive without color (ch. 1).

## 1. Starting from scratch / process

- [ ] The feature was designed from its functionality outward, not from the shell (ch. 1).
- [ ] No UI implies functionality that isn't built (empty "attachments" areas, dead tabs) (ch. 1).
- [ ] The shipped version is the smallest useful one; nice-to-haves are deferred, not half-built (ch. 1).
- [ ] One typeface register, one border-radius policy, consistent copy tone (ch. 1).
- [ ] Values come from defined systems (spacing, type, color, shadow) rather than ad-hoc numbers (ch. 1).

## 2. Hierarchy

- [ ] The primary element is obviously dominant; secondary/tertiary content is visibly quieter (ch. 2).
- [ ] Hierarchy uses weight and color, not only size; no oversized headings or unreadably tiny helper text (ch. 2).
- [ ] At most 2–3 text colors and 2 font weights on the screen (ch. 2).
- [ ] No weights under 400 for small text; de-emphasis uses color/size, not thin weights (ch. 2).
- [ ] No grey or translucent-white text on colored backgrounds; secondary text on color uses a same-hue shade (ch. 2).
- [ ] Where something fails to stand out, its competitors were softened rather than the element inflated (ch. 2).
- [ ] Data is not presented as "label: value" where format or context already identifies it; labels fold into values where possible ("3 bedrooms") (ch. 2).
- [ ] Remaining labels are styled as secondary (smaller/lighter) — unless users scan for labels (spec sheets), in which case labels lead and values are slightly lighter (ch. 2).
- [ ] Section headings in app UIs are small and label-like; heading level does not dictate size (ch. 2).
- [ ] Icons beside text use a softer color than the text (ch. 2).
- [ ] Subtle borders are widened rather than darkened when they need more presence (ch. 2).
- [ ] Buttons: exactly one solid primary; secondaries are outline/low-contrast; tertiaries are link-styled (ch. 2).
- [ ] Destructive actions that are not primary on this page are not big-red-bold; the heavy treatment lives in the confirmation step (ch. 2).

## 3. Layout and spacing

- [ ] Generous white space; the design was trimmed down from "too much", not padded up from cramped (ch. 3).
- [ ] If the UI is dense, that is a documented deliberate choice (ch. 3).
- [ ] All spacing values come from the non-linear scale (16px base, ≥25% steps); no one-off 13px/18px/22px (ch. 3).
- [ ] Every group has more space around it than inside it: label-to-input tighter than group-to-group; more space above headings than below; list gaps larger than line height; same horizontally (ch. 3).
- [ ] Content uses only the width it needs; nothing is stretched to fill 1200–1400px canvases; sections aren't full-width just because the nav is (ch. 3).
- [ ] Fixed-width elements (sidebars, forms, cards) have fixed widths or max-widths; only the main area is fluid; percentages used only where scaling is wanted (ch. 3).
- [ ] No element becomes narrower on large screens than on medium screens (max-width instead of grid columns) (ch. 3).
- [ ] Narrow components in wide layouts use side columns rather than stretching (ch. 3).
- [ ] Mobile layout was designed (≈400px) and large headlines shrink faster than body text; no fixed em ratios driving responsive type (ch. 3).
- [ ] Component size variants tune padding independently of font size (ch. 3).

## 4. Text

- [ ] Font sizes come from a hand-crafted scale in px/rem; no em-based scale; no stray sizes (ch. 4).
- [ ] Typeface: neutral sans or system stack unless the personality calls for more; family has ≥5 weights; no condensed/short-x-height face for body UI (ch. 4).
- [ ] Paragraph width 45–75 characters (20–35em) even inside wider content areas (ch. 4).
- [ ] Line-height suits width and size: ~1.5 narrow, up to 2 wide; taller for small text; ~1 for large headlines (ch. 4).
- [ ] Mixed font sizes on a row share a baseline (ch. 4).
- [ ] Text is left-aligned (for LTR languages); centered text is ≤2–3 lines; justified text has hyphenation (ch. 4).
- [ ] Numeric table columns are right-aligned (ch. 4).
- [ ] Link styling matches context: prose links look clickable; app links use weight/darker color; ancillary links hover-only (ch. 4).
- [ ] All-caps text has increased letter-spacing; headlines in body faces have tightened letter-spacing; headline faces not used small (ch. 4).

## 5. Color

- [ ] Colors are defined in HSL (or tokens derived from an HSL-built palette) (ch. 5).
- [ ] Palette has 8–10 greys (no true black), 5–10 shades for each primary and accent; semantic colors (red/yellow/green) and categorical colors exist where needed (ch. 5).
- [ ] Shades are a fixed 100–900 set; no lighten()/darken()/opacity tricks generating new shades (ch. 5).
- [ ] Light and dark shades are not washed out: saturation increases away from 50% lightness; dark yellows lean orange rather than brown; hue rotations ≤20–30° (ch. 5).
- [ ] Greys share one temperature (cool or warm) across the whole scale, including the lightest and darkest (ch. 5).
- [ ] Normal text ≥4.5:1, large text ≥3:1 (ch. 5).
- [ ] Non-focal colored elements use dark-text-on-light-tint instead of white-on-dark where the dark version would over-emphasize them (ch. 5).
- [ ] Colored text on colored panels gains contrast through hue rotation toward bright hues rather than going white (ch. 5).
- [ ] No information is conveyed by color alone: icons/labels accompany status; chart series differ in lightness (ch. 5).

## 6. Depth

- [ ] Raised elements: lighter top edge, dark sharp shadow below; inset elements: lighter bottom edge, dark inset shadow at the top; light consistently from above (ch. 6).
- [ ] Lighter edges are hand-picked colors, not translucent white (ch. 6).
- [ ] Shadows come from a fixed set (~5) and correspond to z-position: buttons small, dropdowns medium, modals large (ch. 6).
- [ ] Premium surfaces use two-part shadows; the tight ambient shadow fades at higher elevations (ch. 6).
- [ ] Interaction feedback uses elevation (lift on drag, sink on press) (ch. 6).
- [ ] Flat styles still show depth via lighter/darker surfaces or solid no-blur shadows (ch. 6).
- [ ] Overlaps used where layering helps; overlapping images have a background-colored gap (ch. 6).
- [ ] No photo-realistic over-styling (ch. 6).

## 7. Images

- [ ] Photography is professional or high-quality stock; no placeholders awaiting phone photos (ch. 7).
- [ ] Text over images is legible everywhere: overlay, reduced contrast, colorization, or glow shadow applied (ch. 7).
- [ ] Icons displayed near their intended size; large "feature" icons are enclosed in shapes rather than scaled 3–4× (ch. 7).
- [ ] Screenshots are not shrunk to illegibility; partial crops, tablet captures or simplified drawings used (ch. 7).
- [ ] Favicons/small logos are redrawn simplified at target size (ch. 7).
- [ ] User-uploaded images sit in fixed, cropped containers; bleed prevented with inner shadow or translucent inner border, not a solid border (ch. 7).

## 8. Finishing touches

- [ ] Defaults supercharged where appropriate: icon bullets, styled quotes, custom links, brand-colored form controls (ch. 8).
- [ ] Accent borders used to add color where the design is bland (ch. 8).
- [ ] Background decoration (color, ≤30° gradient, pattern, shape) is low-contrast and doesn't hurt readability (ch. 8).
- [ ] Empty states are designed: illustration, emphasized CTA, inert tabs/filters hidden (ch. 8).
- [ ] Borders are the last resort; shadows, background colors and spacing do the separating; redundant borders removed (ch. 8).
- [ ] Components are not boring by default: dropdowns, tables and radio groups considered for richer treatments (ch. 8).

## 9. Systems and tokens (code-level review)

- [ ] Spacing tokens: non-linear, 16px-based, ≥25% between neighbors (ch. 3).
- [ ] Type tokens: hand-picked px/rem; no em scale (ch. 4).
- [ ] Weight tokens: two (normal 400/500, bold 600/700) (ch. 2).
- [ ] Color tokens: grey-100…900, primary-100…900, accents; all authored in HSL (ch. 5).
- [ ] Shadow tokens: ~5 levels, optionally two-part (ch. 6).
- [ ] Radius token policy: one family (none/small/large), never mixed (ch. 1).
- [ ] No magic numbers in component CSS that bypass the tokens (ch. 1).

## 10. Reporting template

```
Screen: <name>            Primary action: <...>        Personality: <serious|playful|...>

Hierarchy      PASS/FAIL  — findings (ch. 2)
Layout/spacing PASS/FAIL  — findings (ch. 3)
Text           PASS/FAIL  — findings (ch. 4)
Color          PASS/FAIL  — findings (ch. 5)
Depth          PASS/FAIL  — findings (ch. 6)
Images         PASS/FAIL  — findings (ch. 7)
Finishing      PASS/FAIL  — findings (ch. 8)
Systems/tokens PASS/FAIL  — findings (ch. 1, 3–6)

Top 3 fixes (highest leverage first — hierarchy and spacing usually come first):
1. ...
2. ...
3. ...
```
