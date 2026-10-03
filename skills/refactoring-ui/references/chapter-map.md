# Chapter map — Refactoring UI (Wathan & Schoger)

Book structure (page numbers from the book's contents) and where each section lives in this skill.
P = principles.md, PB = playbook.md, EX = examples.md, S = scales-and-systems.md,
A = audit-checklist.md.

| Ch. | Section (book page) | P | PB | EX | S | A |
|---|---|---|---|---|---|---|
| 1 Starting from Scratch (6) | Start with a feature, not a layout (7) | ch1 | 1.1 | yes | — | §1 |
| | Detail comes later (10) | ch1 | 1.1 | yes | — | §0, §1 |
| | Don't design too much (13) | ch1 | 1.1 | yes | — | §1 |
| | Choose a personality (17) | ch1 | 1.2 | yes | personality table | §0, §1 |
| | Limit your choices (24) | ch1 | 1.3 | yes | master list, elimination | §1, §9 |
| 2 Hierarchy is Everything (29) | Not all elements are equal (30) | ch2 | 2.1 | yes | — | §2 |
| | Size isn't everything (32) | ch2 | 2.2 | yes | weights/colors | §2 |
| | Don't use grey text on colored backgrounds (36) | ch2 | 2.2, 5.2 | yes | — | §2 |
| | Emphasize by de-emphasizing (39) | ch2 | 2.1 | yes | — | §2 |
| | Labels are a last resort (41) | ch2 | 2.3 | yes | — | §2 |
| | Separate visual hierarchy from document hierarchy (46) | ch2 | 2.4 | yes | — | §2 |
| | Balance weight and contrast (48) | ch2 | 2.1 | yes | — | §2 |
| | Semantics are secondary (52) | ch2 | 2.5 | yes | button table | §2 |
| 3 Layout and Spacing (55) | Start with too much white space (56) | ch3 | 3.1 | yes | — | §3 |
| | Establish a spacing and sizing system (60) | ch3 | 1.3, 3.1 | yes | spacing scale | §3, §9 |
| | You don't have to fill the whole screen (65) | ch3 | 3.2, 3.3 | yes | layout numbers | §3 |
| | Grids are overrated (72) | ch3 | 3.2 | yes | layout numbers | §3 |
| | Relative sizing doesn't scale (79) | ch3 | 3.3 | yes | type scale note | §3 |
| | Avoid ambiguous spacing (83) | ch3 | 3.1 | yes | layout numbers | §3 |
| 4 Designing Text (87) | Establish a type scale (88) | ch4 | 4.1 | yes | type scale | §4, §9 |
| | Use good fonts (94) | ch4 | 4.1 | yes | font filters | §4 |
| | Keep your line length in check (99) | ch4 | 4.2 | yes | text table | §4 |
| | Baseline, not center (102) | ch4 | 4.3 | yes | text table | §4 |
| | Line-height is proportional (105) | ch4 | 4.2 | yes | text table | §4 |
| | Not every link needs a color (109) | ch4 | 4.3 | yes | text table | §4 |
| | Align with readability in mind (111) | ch4 | 4.2, 4.3 | yes | text table | §4 |
| | Use letter-spacing effectively (115) | ch4 | 4.3 | yes | text table | §4 |
| 5 Working with Color (118) | Ditch hex for HSL (119) | ch5 | 5.1 | yes | HSL ref | §5 |
| | You need more colors than you think (123) | ch5 | 5.1 | yes | palette sizes | §5 |
| | Define your shades up front (129) | ch5 | 5.1 | yes | shade construction | §5, §9 |
| | Don't let lightness kill your saturation (133) | ch5 | 5.1 | yes | hue rotation | §5 |
| | Greys don't have to be grey (139) | ch5 | 5.1 | yes | shade construction | §5 |
| | Accessible doesn't have to mean ugly (142) | ch5 | 5.2 | yes | contrast thresholds | §5 |
| | Don't rely on color alone (146) | ch5 | 5.3 | yes | contrast thresholds | §5 |
| 6 Creating Depth (149) | Emulate a light source (150) | ch6 | 6.1 | yes | depth recipes | §6 |
| | Use shadows to convey elevation (158) | ch6 | 6.2 | yes | shadow system | §6, §9 |
| | Shadows can have two parts (163) | ch6 | 6.2 | yes | shadow system | §6 |
| | Even flat designs can have depth (167) | ch6 | 6.3 | yes | depth recipes | §6 |
| | Overlap elements to create layers (170) | ch6 | 6.4 | yes | — | §6 |
| 7 Working with Images (173) | Use good photos (174) | ch7 | 7.1 | yes | — | §7 |
| | Text needs consistent contrast (176) | ch7 | 7.2 | yes | image numbers | §7 |
| | Everything has an intended size (181) | ch7 | 7.3 | yes | image numbers | §7 |
| | Beware user-uploaded content (187) | ch7 | 7.4 | yes | image numbers | §7 |
| 8 Finishing Touches (191) | Supercharge the defaults (192) | ch8 | 8.1 | yes | — | §8 |
| | Add color with accent borders (195) | ch8 | 8.1 | yes | finishing numbers | §8 |
| | Decorate your backgrounds (198) | ch8 | 8.1 | yes | finishing numbers | §8 |
| | Don't overlook empty states (203) | ch8 | 8.3 | yes | — | §8 |
| | Use fewer borders (206) | ch8 | 8.2 | yes | finishing numbers | §8 |
| | Think outside the box (210) | ch8 | 8.1 | yes | — | §8 |
| 9 Leveling Up (215) | Look for decisions you wouldn't have made; Rebuild your favorite interfaces | ch9 | 9 | yes | — | — |

## Image-only content (not recoverable from the text extraction)

- Spacing/sizing scale values (p. 63) — read from the figure by the lead and verified (in S).
- Hand-crafted type scale values (p. 91) — same, verified.
- em-based type scale example (p. 92) — values read from the figure by the lead: .75/.875/1/1.25/1.5em (in S).
- Perceived brightness formula (p. 134) — read from the figure by the lead and verified (in S); the hue-brightness chart (p. 135) is described in words (minima at 0/120/240°, maxima at 60/180/300°).
- The five concrete shadow definitions (p. 161) and the button rest/click shadows (p. 162) — read from the figures by the lead and verified (in S).
- All visual before/after figures — described from surrounding prose in EX.
