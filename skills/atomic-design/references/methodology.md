# Methodology — atoms, molecules, organisms, templates, pages

Source: *Atomic Design* ch. 2 (pp. 38–62) + threads from ch. 1 and ch. 5.
Mental model first: **five stages concurrently working together**, not a linear
process. Use it to think of UIs as cohesive whole and collection of parts at the
same time.

## Origin the book uses

- High-school chemistry (Mr. Rae, balancing equations): atoms combine → molecules
  → organisms. Simplification acknowledged (protons/neutrons exist, but atoms are
  smallest functional unit).
- Periodic tables as proof finite sets compose infinite outcomes: chemical elements;
  Josh Duck's Periodic Table of HTML Elements (all sites/apps/intranets from same
  HTML elements).
- Borrowed from industrial design/architecture (airplanes, ships, skyscrapers) and
  OOP (separation of concerns, single responsibility) — not invented ex nihilo.

## The five stages

### 1. Atoms — foundational, indivisible, abstract
- What: basic HTML tags that can't break further without losing function: form
  label, input, button, h1, paragraph, image, icon, color, font.
- Properties matter: hydrogen (1 electron, flammable — Hindenburg) vs helium
  (2, inert). UI parallel: hero-image dimensions, primary-heading font-size condition
  how the atom may be applied.
- In library: base-styles glanceable reference. Don't present alone as design —
  atoms "don't exist in a vacuum, only come to life with application."
- Test: if you can split it and both halves still function as UI, it isn't an atom.

### 2. Molecules — simple functional groups, one job
- What: 2+ atoms bonded with distinct new properties. Chemistry parallel: H2O vs
  H2O2 — same atoms (H, O), wildly different behavior.
- Canonical example: search-form molecule = label atom + input atom + button atom.
  Alone abstract; together: label defines input, button submits — portable, reusable,
  droppable anywhere search is needed.
- Discipline payoff: single responsibility ("do one thing well"). Simple molecules →
  easier testing, reusability, consistency. Don't burden one pattern with complexity
  or software gets unwieldy.
- Test: can you name its job in 3 words? Can you drop it elsewhere unchanged?

### 3. Organisms — distinct sections in context
- What: groups of molecules and/or atoms and/or other organisms forming a section.
- Heterogeneous example: header organism = logo atom + primary-nav molecule +
  search-form molecule + utility nav. Seen on almost every site.
- Homogeneous example: product grid organism = same product-item molecule repeated
  (Gap category page; also search results, related products).
- Payoff: context. Small simple components shown in action; reusable sections
  ("product grid anywhere a group of products displays").
- Test: can you point to it on a page as "the header / the grid" without pointing
  inside it?

### 4. Templates — layout + content structure, not final content
- What: page-level objects placing components in layout, articulating underlying
  content structure. Chemistry analogy ends here — use client-safe language.
- Example: homepage template = header organism + hero + sections + footer in layout.
  Time Inc. homepage template shows components functioning together + declares image
  sizes and headline/text character lengths.
- Boulton rule: "You can create good experiences without knowing the content.
  What you can't do is create good experiences without knowing your content
  structure. What is your content made from, not what your content is."
- Payoff: proves parts add to functioning whole; guardrails for dynamic content
  (what fits where). Skeleton before meat.
- Test: could a CMS fill it with different articles/products tomorrow and still hold?

### 5. Pages — specific instances with real content, most concrete
- What: template + real representative text/images/media.
- Example: homepage template → homepage page: hero "Lorem Ipsum"+FPO becomes
  "Moving People"+Beyoncé image. This is what users touch, stakeholders sign, and
  where you see components forming beautiful functional UI.
- Payoff: tests effectiveness of system against reality; reveals where structure
  fails content (overflows, orphans, gaps). Page reality feeds back into atoms.
- Frost loop: content poured into pages influences molecules/organisms/templates —
  adjust upstream, not just hotfix the page.

## How to work the levels together

- **Part-and-whole traversal:** painter steps back from easel to assess, steps in to
  detail. Zero in on atom/molecule to fix ("header's broken!") while seeing page
  impact; zoom out to page/template to judge composition.
- **Taxonomy discipline:** give the five labels to colleagues/vendors; spend the
  naming conversation once ("Principles/Basics/..." variants allowed) so every later
  discussion inherits the language. Teams that share "Blocks Three-Up" (Starbucks)
  stop talking past each other.
- **Beyond marketing pages:** same hierarchy for native mobile (Instagram organisms
  dissected in book), dashboards, intranets — "atomic design is for user interfaces,"
  born of the web but not bound to it.
- **Don't over-extend chemistry:** clients/bosses/colleagues hear templates/pages,
  not "let's discuss our organisms." Trust Frost: carrying chemistry too far makes
  you sound crazy.

## Common misclassifications

- Button with icon + label: molecule (two atoms), not atom — unless your system
  defines icon-button as indivisible base (then document why).
- Header with only a logo: still organism (section role), not molecule — role, not
  size, decides.
- Template with lorem: still template until representative content lands. FPO +
  grayscale + limits = structure signal, not page proof.
- Two similar cards with different content: one card organism/molecule with data
  variation, not two patterns — reach for pseudo-patterns (see patternlab.md).
