---
name: color-interaction-albers
description: >
  Josef Albers' Interaction of Color (1963) as practical color judgment. Use it whenever
  someone is choosing, comparing, or reviewing color and wants perception-correct
  decisions: "this color looks different here / wrong / muddy / vibrating", "make this
  look the same / different on purpose", "text on color unreadable", "palette /
  tokens / greys / scales", "transparency / layering / boundaries", "quantity /
  placement / harmony", "critique this screen / palette / data-viz". Applies even when
  Albers is not mentioned. Paper studies transfer to screens; screen-only thresholds
  (e.g. WCAG ratios) are marked extractor notes in references, not Albers' own words.
---

# Interaction of Color — seeing and judging color in context

This skill gives you Albers' working method: **color is the most relative medium in
art — almost never seen as it physically is** (Intro, ch. IV). Operationally: never
judge a swatch in isolation; compare candidates side by side on the actual ground,
in the actual quantity, at the actual size; deceive on purpose in studies so you are
not deceived by accident in production; practice before theory (systems last).

Source fidelity: Josef Albers, *Interaction of Color: text of the original edition
with selected plates* (Yale 1963; paperback 1971, 108 pp. scan). Roman-numeral
chapters I–XXVI below are the book's. Screen/UI transfer lives only in
`references/apply-to-ui.md` and is marked as derived, never as Albers' words.
See `references/chapter-map.md` for chapter-to-file mapping and image-dependent gaps.

## Workflow

Use the same loop whether choosing a token, fixing a screen, or running a critique.

1. **State the actual fact wanted.** What should the user *see* (same? different?
   lighter? receding? calm?), not the hex. A hex is a factual fact; perception is
   the actual fact (ch. XXV).
2. **Compare, don't stare.** Put 2–4 candidates on the real ground, at real size and
   quantity. Single-color staring fatigues the eye and invites after-image error
   (ch. VIII). Procedure in `references/playbook.md` B1–B3.
3. **Run the deception test.** Can you make one color look like two (reversed
   grounds, ch. VI), or two look alike (subtraction, ch. VII)? If yes, you control
   the influence; if no, the context controls you.
4. **Check the four confounders.** Light intensity vs color intensity (ch. V);
   boundaries vibrating/vanishing (ch. XXII–XXIII); mixture/transparence reading
   (ch. IX–XI); quantity/placement/recurrence (ch. XVI). Details in playbook B4–B6.
5. **Transpose and re-see.** Move the palette to another key / ground / scale
   (ch. XIV); view at distance, small, and in grayscale. What breaks is what the
   context was hiding.
6. **Critique Albers-style.** Exhibition of trials, one problem at a time, judgment
   by comparison, vocabulary discipline (see `references/teaching-and-critique.md`
   + playbook B8). Theory and systems only at the end (ch. XXIV).

Key questions to keep asking: *On what ground, in what quantity, next to what?
Am I judging the swatch or the seeing? Which influence am I using — and which is
using me? Does it still hold reversed, smaller, farther, grey?*

## Core rules (atomic skills)

Each rule is one concrete ability. Book chapter in parentheses.

Foundations (Intro, I–II, XXV)
1. Treat every color judgment as contextual: "almost never seen unconnected and
   unrelated" (ch. II). No isolated-swatch approvals.
2. Separate factual fact (wavelength/hex, fixed) from actual fact (what acts in
   time: transparent-read, 3-as-4, vibrating/vanishing). Design for the actual.
3. Prefer *Schauen* (seeing + imagination) over fact-collecting: what matters is
   the how (action), not the what (identification) — Kandinsky via ch. II.
4. Practice before theory: run paper/screen trials first; teach systems (Munsell,
   Ostwald, Goethe triangle, ch. XXIV) last when eyes are prepared.
5. Distrust visual memory: color recollection is poor (ch. I, Coca-Cola test).
   Compare live, never from memory.

Relativity and influence (IV, VI–VII)
6. Demonstrate "one color has many faces": place the identical middle color on
   clearly lighter vs darker grounds to split its reading (ch. IV tile pattern,
   IV-3, three-pots analogy).
7. Make 1 color appear as 2 with reversed grounds: find two grounds that pull one
   middle color apart (ch. VI, playbook A6).
8. Make 2 different colors look alike by subtraction: choose grounds that cancel
   their difference (ch. VII, three reds; playbook A7). Use to harmonize, or to
   detect accidental harmonizing.
9. Name the interaction correctly: mutual influencing = interaction; viewed as
   dependence = interdependence (ch. XXV). Extends across senses (tone, appetite).

After-image — the root cause (VIII, XII, XV)
10. Predict simultaneous contrast: staring at red then white yields green
    after-image; every ground tints its neighbor toward its complement
    (ch. VIII, red/white circles VIII-2).
11. Rest the eye between comparisons; never decide after prolonged staring at one
    color. Fatigue manufactures difference.
12. Use optical mixture deliberately (Impressionists, ch. XII) vs accidental
    muddiness: small juxtaposed touches fuse at distance; large areas don't.

Light, intensity, scales (V, XIV, XX, XXV terms)
13. Distinguish light intensity (how light/dark) from color intensity (how
    bright/saturated): a yellow can be lighter yet more intense than a dark blue
    (ch. V, Ensor/Mondrian cases).
14. Decide darker/lighter by after-image + independent tests, not by feeling:
    self-test protocol (playbook A2–A3, B2).
15. Build even gradations by Weber-Fechner: equal physical steps look unequal —
    middle steps need widening (Chevreul rows, pool steps, ch. XX; playbook A19, B4).
    Never trust linear ramps.
16. Sort one hue by intensity before composing: lightest↔strongest ordering reveals
    gaps duplicates can't fill (ch. V, playbook A5).
17. Transpose palettes by intervals, not by hex math: keep interval relationships
    when moving to another key ("Good morning" exchange, ch. XIV; playbook A12, B7).

Mixture, transparence, space (IX–XI, XV)
18. Produce illusionary transparence in opaque media: choose the middle mixture so
    flat colors read as overlapping films (cover XVII-1, ch. IX; playbook A9).
19. Separate factual mixtures (additive light / subtractive pigment, ch. X) from
    perceived mixture (what the eye reports). Don't explain perception with tube
    math.
20. Control space-illusion with middle-mixture placement: boundaries' softness/
    hardness signals nearness/distance (ch. XI, Cézanne, three hands; playbook A11, B5).
21. Read intersecting colors / fluting: two overlapping fields generate a third
    read (XV-2 sliding red; playbook A13). Use for layering, watch for accidental
    depth.

Boundaries (XI, XX, XXII–XXIII)
22. Kill or keep vibration on purpose: equal-intensity complementary neighbors
    vibrate (ch. XXII, playbook A20). To calm, separate with a boundary (dark,
    light, or neutral line) or shift one side in lightness.
23. Dissolve or assert form with equal-light-intensity: matched lightness erases
    contours (clouds, XXIII-2; playbook A21) — legibility dies before hue contrast
    does. Check in grayscale.
24. Specify every boundary: hard (cut edge), soft (gradient), or line-separated.
    Unspecified edges default to the worst of the three.

Optical mixture and Bezold (XII–XIII)
25. Predict the Bezold effect: changing one color alone re-tunes the whole
    combination (Bezold rugs, ch. XIII). Re-test the set after any single-token change.
26. Choose juxtaposition size with intent: fine stripes fuse (playbook A16), broad
    fields contrast. Same colors, opposite readings.

Harmony, quantity, recurrence (XVI, XXIV)
27. Compose by quantity, not just hue: four performances of one cast (same colors,
    different amounts/placements = different harmonies, ch. XVI; playbook A14, B6).
    Small accents dominate; large fields absorb.
28. Place and repeat deliberately: recurrence steadies, isolation excites; interiors
    demo in book shows placement outweighing palette.
29. Distrust hue-circle harmony rules alone: Goethe triangle and system harmonies
    (ch. XXIV) never substitute for eye trials (playbook A22 last, not first).
30. Prefer variants over variety: related transformations of one idea beat many
    unrelated ideas (ch. XXV). Variety without relation is noise.

Film, volume, temperature (XVII, XXI)
31. Distinguish surface color from film/volume color: coffee, pool water, mountains —
    colors seen *through* or *as* volume behave differently from opaque surfaces
    (ch. XVII). Glassy/overlay UI reads as film, not paint.
32. Use temperature relativistically: warm/cool exists only by comparison; Boucher
    vs Rubens show same hue flipping role (ch. XXI). No absolutely warm blue.
33. Name humidity/dryness and other polarities only as comparisons, never as swatch
    properties (ch. XXI).

Media, masters, free work (III, XVIII–XIX)
34. Work with swatches not mixtures when studying: color paper (or digital swatch
    library) forces "just the right color" by comparison; paint/pickers hide poor
    conception in mixing/texture (ch. III; playbook A0). Avoid tuned failure-proof sets.
35. Copy the masters by re-performance, not by eyedropper: rebuild their color
    instrumentation (selection + presentation) in your medium (ch. XIX; playbook A18).
36. Schedule free studies: stripes (restricted juxtaposition), fall leaves (found
    color), open themes (ch. XVIII; playbook A15–A17) — taste and invention need
    unconstrained trials alongside controlled ones.

Critique discipline (XXV + teaching file)
37. Bring admission tickets: every participant shows trials, not opinions
    (ch. XXV).
38. Judge by comparison in exhibition: trials side by side, one problem at a time,
    group sees together before speaking (playbook B8).
39. Enforce vocabulary: actual vs factual, light vs color intensity, interaction vs
    harmony — sloppy terms hide sloppy seeing (glossary.md).

## When to read which reference

| Task | Read |
|---|---|
| Need laws with conditions + pitfalls | `references/principles.md` (§1–15 by topic) |
| Need step-by-step trials A0–A22 or task protocols B1–B8 | `references/playbook.md` |
| Need UI/screen transfer (tokens, text-on-color, data-viz, states, scales, layering, layout) | `references/apply-to-ui.md` (§1–12 + checklist) |
| Need book cases to cite or copy | `references/examples.md` |
| Need chapter→skill map, edition + image gaps | `references/chapter-map.md` |
| Need terms in Albers' sense (actual/factual, cast, fluting, Bezold) | `references/glossary.md` |
| Need critique session script, teaching order, taste | `references/teaching-and-critique.md` |
| Quick calls: compare colors / darker test / same-or-different / scales / boundaries / quantities / transposition / critique | playbook B1–B8 |

## Anti-patterns Albers calls out

- Approving swatches in isolation (picker, token file) then surprised on the ground (ch. II, IV).
- Trusting visual memory across meetings ("Coca-Cola red from memory," ch. I).
- Explaining perception with tube/wavelength math; acoustics-knowledge fallacy —
  system knowledge ≠ sensitivity (Intro, ch. X, XXIV).
- Theory-first teaching: color systems before eyes are prepared (ch. XXIV–XXV).
- Prepared/tuned sets guaranteeing success; texture or mixing hiding conception (ch. III).
- Best-case-only palettes: one ground, one size, one quantity — then Bezold,
  vibration, or vanishing breaks production (ch. XIII, XXII–XXIII, XVI).
- Linear ramps presented as even scales (Weber-Fechner violation, ch. XX).
- Hue-only harmony: circle rules without quantity/placement/recurrence trials (ch. XVI, XXIV).
- Confusing light intensity with color intensity; grayscale-blind approvals (ch. V, XXIII).
- Unspecified boundaries defaulting to accidental vibration or dissolution (ch. XXII–XXIII).
- Variety over variants: many unrelated ideas instead of related transformations (ch. XXV).
- Critique by opinion and jargon instead of exhibited trials + disciplined terms (ch. XXV).
