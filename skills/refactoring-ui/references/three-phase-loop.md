# Three-phase UI refactoring loop (Constrain → Focus → Balance)

Source: `Refactoring_UI_Blueprint.pdf`, a 13-slide companion deck derived from the book
("Refactoring UI: Geliştiriciler ve Tasarımcılar İçin Pratik Arayüz Kuralları"). It adds no new
rules beyond the book; its value is a compact loop for refactoring an *existing* screen.
Every item below maps to a book section (chapter in brackets) — read the book-based references
when you need the reasoning or the numbers.

Use this when someone says "this screen looks off / amateurish / cluttered, fix it" and you want
a disciplined pass instead of random tweaks. Run the loop until a pass changes nothing.

## Phase 1 — Constrain (Sınırlandır) [ch. 1 "Limit your choices", ch. 3, ch. 4, ch. 5]

Design is not unlimited freedom; infinite options cause decision fatigue. Good design is a
system of constraints: decide the values once, then pick from the pool for every new decision.

- [ ] Are colors and fonts drawn from a predefined system (e.g. CSS custom properties such as
      `--font-size-small/medium/large/xlarge: 14/16/20/24px`, `--color-primary/secondary/neutral`)
      rather than a color wheel and a font dropdown?
- [ ] Is there a spacing/sizing scale (8px-grid style: consistent padding, aligned edges)?
- [ ] Is the shade pool fixed (e.g. "pick one of these 8 blues") instead of continuous?
- [ ] Does the design still work in black and white? Working in grayscale first forces you to
      use size, spacing and contrast for hierarchy; color comes later as a bonus [ch. 1
      "Design in grayscale"].

Personality matrix (pick one deliberately) [ch. 1 "Choose a personality"]:

| | Serious / professional | Playful / friendly |
|---|---|---|
| Typography | elegant serif (e.g. Freight Text) | rounded sans (e.g. Proxima Soft) |
| Colors | navy `#003366`, gold `#D4AF37` | pink `#FF00FF`, cyan `#00FFFF` |
| Corners | `border-radius: 0` | `border-radius: 999px` (pill) |

## Phase 2 — Focus (Odaklan) [ch. 1 "Start with a feature, not a layout", ch. 2]

"Designing an app" is not designing the shell. Put the core feature in the center and let the
shell (navigation, layout) be shaped by the feature's needs — not "should the nav be left or
right?" first.

- [ ] Is the screen designed around the core function, not decoration?
- [ ] Were distracting, competing secondary elements pushed to the background? Instead of
      enlarging the active item, fade the inactive ones (de-emphasize to emphasize) [ch. 2
      "Emphasize by de-emphasizing"].
- [ ] Hierarchy toolkit: size (16 → 24px), weight (400 → 700), color (soft grey → punchy brand
      color). Instead of making a price huge: keep size small, raise weight, darken color
      [ch. 2 "Size isn't everything"].
- [ ] Labels are a last resort: if the data format or context already says what it is
      (`12 items left in stock`, `3 🛏 bedrooms`), drop the `Stock: 12` label and let the data
      speak [ch. 2 "Labels are a last resort"].
- [ ] Semantic ≠ visual hierarchy: an `<h1>` is a structural requirement, not a size mandate.
      Section titles are usually labels, not focal points — a 16px `h1` over tabs can be right
      [ch. 2 "Don't let semantics dictate style"].

## Phase 3 — Balance (Dengele) [ch. 2 "Balance weight and contrast", "Don't use grey text on colored backgrounds"]

- [ ] Grey text on colored backgrounds? Don't lower opacity (the background bleeds through and
      muddies the text). Hand-pick a lighter / less saturated tone of the background hue in HSL.
- [ ] Weight vs contrast: thin strokes need high contrast; heavy strokes / large surfaces need
      *lower* contrast (reduce color intensity) to avoid looking harsh. As surface area grows,
      drop contrast — this inverse relation is the key to visual harmony.
- [ ] After removing redundant labels, does the data read on its own?

## Exit check

Good UI is not magic; it is this loop applied with discipline. Stop when: every value comes
from the system, the core feature is the obvious focal point, and no element shouts louder
than its importance.
