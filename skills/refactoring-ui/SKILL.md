---
name: refactoring-ui
description: >
  Practical visual UI design for developers, distilled from "Refactoring UI" (Adam Wathan &
  Steve Schoger). Use it whenever someone is building, styling, reviewing or fixing a user
  interface and wants it to look professionally designed without a designer: "make this look
  better / less amateurish / more polished", "why does my UI look off", "review this screen /
  component / landing page / dashboard / form", "pick fonts / colors / spacing / shadows",
  "set up design tokens or a Tailwind/CSS theme", "build a color palette", "fix hierarchy",
  "this looks cluttered / flat / boring", "text on an image is unreadable", "empty state",
  "button styles", "card / modal / dropdown design", "responsive sizing", "accessible but not
  ugly colors". Also triggers for design-system setup (spacing scale, type scale, shade scales,
  elevation levels), UI audits and PR reviews that touch CSS/styling, and for choosing a visual
  personality for a new product. Applies even when the book is not mentioned.
---

# Refactoring UI — design skill for developers

This skill gives you the authors' working method: good-looking interfaces come from **visual
hierarchy, constrained systems and disciplined spacing**, not from artistic talent. Operationally:
start from a feature rather than a shell; design in grayscale so contrast, size and spacing do the
work; replace every open-ended choice (font size, shade, shadow, margin) with a small predefined
scale; de-emphasize the unimportant before emphasizing the important; and only then add color,
depth, imagery and finishing touches. Every rule below carries the book's numbers so it can be
applied directly in CSS or design tokens.

## Workflow

Use the same loop whether you are creating a screen, reviewing one, or fixing one.

1. **Frame the task.** Which feature is this (not "the app")? What is the single primary action
   and the primary content? What personality is intended (serious/formal vs playful/friendly)?
   What systems already exist (spacing, type, color, shadow tokens)? If none, define them first
   (see `references/scales-and-systems.md`).
2. **Audit hierarchy in grayscale.** Mentally (or literally) remove color. Can you tell primary
   from secondary from tertiary by size, weight, color-lightness and spacing alone? If not, fix
   hierarchy before anything else — it is the highest-leverage change.
3. **Fix spacing and layout.** Start with too much white space and remove; snap all values to the
   spacing scale; ensure more space around groups than within; use only the width content needs;
   fix widths where fluid grids misbehave.
4. **Fix text.** Snap to the type scale; two weights; 45–75 character lines; line-height by width
   and size; baseline alignment; alignment and letter-spacing rules.
5. **Apply color.** Build or use the shade scales (greys 8–10, primary 5–10, accents); use HSL;
   correct saturation at the ends; check contrast (4.5:1 / 3:1) and never color-only meaning.
6. **Add depth.** Light from above; shadows from a ~5-level elevation set tied to z-position;
   overlap for layering.
7. **Handle images, then finishing touches.** Text-on-image contrast, intended sizes, user
   uploads; then icon bullets, accent borders, background decoration, empty states, fewer borders.
8. **Report or ship.** For reviews, walk `references/audit-checklist.md` top to bottom and
   return findings per chapter with the top three fixes. For builds, verify every value maps to a
   system token.

Key questions to keep asking: *What is the one primary thing here? What can I de-emphasize? Is
this value on a scale? Is there more space around the group than inside it? Would this still read
correctly in grayscale? Does the shadow match the element's z-position?*

## Core rules

Process and systems (ch. 1)
1. Start with a feature, not a layout; design the shell after a few features exist.
2. Work low-fidelity first (paper, thick marker), defer typeface/shadow/icon decisions, and design
   in grayscale before adding color.
3. Build in short cycles: simple version → make it real → iterate → next feature; never design
   every edge case in the abstract, and never imply functionality you won't build now.
4. Personality is set by four levers: typeface (serif elegant / rounded sans playful / neutral
   sans plain), color (blue safe, gold expensive, pink fun), border radius (none formal / small
   neutral / large playful — never mixed), and copy tone.
5. Limit choices with predefined systems for font size, weight, line height, color, margin,
   padding, width, height, shadows, radius, border width, opacity. Choose by elimination: guess,
   compare the two neighbors, repeat.

Hierarchy (ch. 2)
6. Control hierarchy with weight and color, not size alone: 2–3 text colors (dark, grey, lighter
   grey) and 2 weights (400/500 normal, 600/700 bold). No weights under 400 for UI text.
7. On colored backgrounds never use grey or translucent white; hand-pick a same-hue color with
   adjusted saturation/lightness.
8. Emphasize by de-emphasizing: soften the competitors (inactive nav items, sidebar backgrounds)
   instead of inflating the hero.
9. Labels are a last resort: rely on format/context, fold labels into values ("3 bedrooms"), style
   remaining labels as secondary — unless users scan for labels (spec sheets).
10. Semantic markup never dictates size: an h1 page title can be small; section titles are labels.
11. Balance weight and contrast: soften heavy icons with lower contrast; thicken too-faint borders
    instead of darkening them.
12. Buttons follow the action pyramid: one solid primary, outline/low-contrast secondaries,
    link-style tertiaries; destructive gets big-red-bold only where it is primary (the
    confirmation step).

Layout and spacing (ch. 3)
13. Start with too much white space and remove it; dense layouts are a deliberate exception.
14. Spacing/sizing scale: 16px base, non-linear, adjacent values at least ~25% apart
    (book's scale: 4 8 12 16 24 32 48 64 96 128 192 256 384 512 640 768).
15. More space around a group than within it (labels closer to their inputs than to the next
    group; more space above a heading than below).
16. Use only the width content needs; fixed widths/`max-width` for sidebars, cards and forms;
    fluid only for main areas; never let a card be narrower on large screens than on medium.
17. Relative sizing doesn't scale: large text shrinks faster than small (45px/18px desktop →
    20–24px/14px mobile); size component padding independently of font size; design at ~400px
    first.

Text (ch. 4)
18. Hand-crafted type scale in px/rem, never em (book's scale: 12 14 16 18 20 24 30 36 48 60 72).
19. Fonts: neutral sans or the system stack; reject families with fewer than 5 weights (Google
    Fonts "styles ≥ 10"); avoid condensed/short-x-height faces for body UI; sort by popularity.
20. Line length 45–75 characters (20–35em). Line-height ~1.5 narrow, up to 2 wide; taller for small
    text, ~1 for large headlines.
21. Align mixed sizes by baseline; left-align body text; center only ≤2–3 lines; right-align
    numbers; hyphenate justified text; add letter-spacing to all-caps; tighten it on headlines set
    in body faces.
22. In link-dense UIs emphasize links by weight/darker color, hover-only for ancillary links.

Color (ch. 5)
23. Use HSL. Palette: greys 8–10 shades (no true black), 1–2 primaries × 5–10, accents (attention,
    red/yellow/green semantic, categorical) × multiple shades; up to ~10 colors.
24. Define shades up front as a 100–900 scale: base 500 (button background), 900 text, 100 tint,
    then 700/300, then the rest. No lighten()/darken() at use sites.
25. Raise saturation as lightness leaves 50%; change brightness by rotating hue toward 60/180/300°
    (lighter) or 0/120/240° (darker), max 20–30°. Tint greys warm or cool and keep the temperature
    at both ends.
26. Contrast ≥4.5:1 normal text, ≥3:1 large; flip to dark-text-on-light-tint when white-on-dark
    over-emphasizes; rotate hue toward bright hues for colored-on-colored text; never rely on color
    alone (icons, lightness differences).

Depth (ch. 6)
27. Light comes from above: raised = lighter top edge + small sharp dark shadow below; inset =
    lighter bottom edge + dark inset shadow at the top. Hand-pick highlight colors.
28. Fixed elevation set (~5 shadows) assigned by z-position (button small, dropdown medium, modal
    large); two-part shadows (soft cast + tight ambient, ambient fading with height); lift on drag,
    sink on press.
29. Flat designs convey depth with lighter-is-closer surfaces, solid no-blur shadows and
    overlapping elements (background-colored gaps between overlapping images).

Images (ch. 7)
30. Use professional or quality stock photos; never placeholders awaiting phone shots.
31. Text on images: overlay (black for light text, white for dark), lower image contrast, colorize
    (contrast ↓, desaturate, multiply fill), or a glow text-shadow (big blur, no offset).
32. Respect intended sizes: no 3–4× icon upscaling (enclose in a shape instead), no ~70%
    screenshot shrinking (tablet capture, partial crop or simplified drawing), redraw favicons.
33. User uploads: fixed cropped containers (`background-size: cover`); inner shadow, not borders,
    against background bleed.

Finishing touches (ch. 8–9)
34. Supercharge defaults (icon bullets, big colored quotes, custom underlines, brand-colored
    checkboxes); add accent borders; decorate backgrounds at low contrast (gradients ≤30° hue
    apart, patterns, shapes).
35. Design empty states as the first impression: illustration + strong CTA; hide inert tabs and
    filters.
36. Use fewer borders: box-shadows, distinct background colors, or spacing instead.
37. Rethink boring components (dropdown panels, merged table columns, radio groups as cards).
38. Keep learning: note decisions you wouldn't have made; rebuild favorite UIs without dev tools.

## When to read which reference

| Task | Read |
|---|---|
| Set up design tokens / Tailwind theme / spacing, type, color, shadow scales | `references/scales-and-systems.md` (all numbers), playbook §1.3 |
| Review or audit a screen, component or styling PR | `references/audit-checklist.md`, then playbook §10 symptom table |
| Build a new feature or product from zero | playbook §1 (process, personality, systems) |
| "It looks cluttered / flat / nothing stands out" | playbook §2 (hierarchy) and §3 (spacing); principles ch. 2–3 |
| Buttons, actions, destructive flows | playbook §2.5; principles "Semantics are secondary" |
| Displaying data, dashboards, spec sheets, labels | playbook §2.3; examples "Label: value cards" |
| Typography choices, paragraphs, tables, links, caps | playbook §4; scales "Line length, line-height…" |
| Build a palette, shades, greys, accessible color | playbook §5; scales "Shade scale", "Hue rotation", "Contrast" |
| Shadows, raised/inset controls, flat depth, overlaps | playbook §6; scales "Shadow / elevation", "Depth recipes" |
| Hero images, icons, screenshots, avatars | playbook §7; scales "Image numbers" |
| Polish a correct-but-plain design; empty states; too many borders | playbook §8; examples "Finishing touches" |
| Need the author's reasoning or a definition | `references/principles.md` (by chapter) + glossary |
| Need a concrete before/after to explain a recommendation | `references/examples.md` |
| Map a book chapter/page to this skill, or see what was image-only | `references/chapter-map.md` |
| Quick 3-phase refactoring pass (constrain → focus → balance) on an existing screen | `references/three-phase-loop.md` |

## Anti-patterns the authors call out

- Designing the navigation/shell first; designing every feature and edge case before building;
  mockups that imply unbuilt features (ch. 1).
- Nudging values one pixel at a time (12 vs 13px, 10% vs 15% shadow) instead of using a scale;
  mixing square and rounded corners (ch. 1).
- Size-only hierarchy; thin (<400) weights for small text; grey or translucent-white text on
  colored backgrounds; `label: value` for everything; huge h1s because "h1 should be big";
  every button solid and bold; red-bold destructive buttons outside confirmation (ch. 2).
- Adding white space only until it stops looking bad; linear "multiples of 4" scales; equal
  gaps inside and around groups; filling 1400px canvases; fluid-grid sidebars; cards that shrink
  on large screens; em-driven responsive type; padding scaled from font size (ch. 3).
- Every size from 10–24px in use; em-based type scales; fonts with few weights; condensed faces
  for body text; lines over 75 characters; vertical-centering mixed sizes; centered paragraphs;
  justified text without hyphenation; link-blue everywhere; untracked all-caps (ch. 4).
- Hex/RGB thinking; five-color generator palettes; true black greys; shades computed on the fly;
  washed-out tints and muddy darks; hue rotations beyond 20–30°; white-on-dark for every badge;
  color as the only signal (ch. 5).
- Shadows without an elevation logic; translucent-white highlights; photo-realistic over-styling;
  flat designs with no depth cues; overlapping images that clash (ch. 6).
- Placeholder photos; unreadable hero text; upscaled icons; downscaled screenshots and favicons;
  uncontrolled user image sizes; borders to fix bleed (ch. 7).
- Browser-default bullets/controls when polish is wanted; high-contrast background decoration;
  ignored empty states with dead tabs/filters; borders as the default separator; dropdowns,
  tables and radios that are "just the default" (ch. 8).
