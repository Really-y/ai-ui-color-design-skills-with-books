# AI UI, UX & Color Design Skills from Foundational Books 🎨📚

> **Every foundational UI/UX, color theory, and product design book has been comprehensively read, distilled, and transformed into operational AI agent skills powered by Claude Fable 5.1.**

[![GitHub Repository](https://img.shields.io/badge/GitHub-ai--ui--color--design--skills--with--books-blue?logo=github)](https://github.com/Really-y/ai-ui-color-design-skills-with-books)
[![Synthesized with](https://img.shields.io/badge/Synthesized%20with-Claude%20Fable%205.1-purple.svg)](https://anthropic.com)
[![Target Agents](https://img.shields.io/badge/Compatible%20with-Antigravity%20%7C%20Claude%20Code%20%7C%20Cursor-success.svg)]()

---

## 📖 About The Project

Modern AI coding agents frequently struggle with user interface aesthetics, visual hierarchy, color perception, and usability conventions because generic training data emphasizes code syntax over design philosophy.

To bridge this gap, this repository provides a structured, battle-tested collection of **AI Agent Skills**. Each skill represents a complete, deep-dive synthesis of a seminal design book. Using **Claude Fable 5.1**, each book was read end-to-end, broken down into its core principles, and transformed into actionable rules, audit checklists, and step-by-step playbooks ready for immediate deployment in agentic workflows.

---

## 📚 Books & Skills Catalog

| Book & Author | Skill Directory | Core Focus & Methodology |
| :--- | :--- | :--- |
| **Refactoring UI**<br>*Adam Wathan & Steve Schoger* | [`skills/refactoring-ui`](./skills/refactoring-ui) | Developer-first tactical design. 8-pt spacing grids, grayscale-first design loops, typography scales, contrast, elevation/shadows, and practical UI layout patterns. |
| **The Elements of User Experience**<br>*Jesse James Garrett* | [`skills/ux-five-planes`](./skills/ux-five-planes) | Garrett's 5 UX Planes framework: **Strategy → Scope → Structure → Skeleton → Surface**. Complete product planning, information architecture, interaction design, and layer diagnostics. |
| **Don't Make Me Think, Revisited**<br>*Steve Krug* | [`skills/web-usability-krug`](./skills/web-usability-krug) | Web and mobile usability engineering. Designing for scanning, elimination of cognitive friction, Trunk Test audits, DIY usability test kits, and radical clarity. |
| **The Design of Everyday Things**<br>*Don Norman* | [`skills/design-of-everyday-things`](./skills/design-of-everyday-things) | Human-Centered Design (HCD). Affordances, signifiers, mappings, feedback, conceptual models, 7 stages of action, and resilient error recovery. |
| **Interaction of Color**<br>*Josef Albers* | [`skills/color-interaction-albers`](./skills/color-interaction-albers) | Color relativity and perception. Simultaneous contrast, lightness/saturation illusions, UI palette harmony, accessible color relationships, and visual weight. |
| **Atomic Design**<br>*Brad Frost* | [`skills/atomic-design`](./skills/atomic-design) | Design system mental models: **Atoms → Molecules → Organisms → Templates → Pages**. Decoupling structure from content, Pattern Lab mechanics, and pseudo-patterns. |
| **Atomic Design Systems**<br>*Brad Frost Methodologies* | [`skills/atomic-design-systems`](./skills/atomic-design-systems) | Interface inventory execution, component classification workflows, pattern libraries, and design system governance. |

---

## 🛠️ Repository Structure

Every skill is self-contained with explicit operational trigger definitions, rules, checklists, and references:

```text
skills/
├── atomic-design/
│   ├── SKILL.md                          # Main instructions, triggers & core rules
│   └── references/                       # Chapter map, glossary, methodology, patternlab, principles
├── atomic-design-systems/
│   └── references/                       # Classify component, interface inventory, principles
├── color-interaction-albers/
│   ├── SKILL.md                          # Josef Albers color theory & UI application rules
│   └── references/                       # Apply to UI, examples, principles, critique
├── design-of-everyday-things/
│   ├── SKILL.md                          # Don Norman's cognitive ergonomics & interaction playbook
│   └── references/                       # Diagnose interaction, design for error, playbook
├── refactoring-ui/
│   ├── SKILL.md                          # Tactical visual design guidelines & UI checklists
│   └── references/                       # Scales and systems, audit checklist, three-phase loop
├── ux-five-planes/
│   ├── SKILL.md                          # 5-stage UX planning, information architecture & wireframing
│   └── references/                       # Planes checklist, playbook, glossary
└── web-usability-krug/
    ├── SKILL.md                          # Steve Krug's usability laws & scanning principles
    └── references/                       # Trunk test, usability test kit, playbook, principles
```

---

## 🚀 How to Use

### 1. Antigravity CLI / Google Agentic Workspaces
To install these skills globally into your Antigravity agent environment:
```bash
# Copy all skills to Antigravity's global skills directory
mkdir -p ~/.gemini/antigravity-cli/skills
cp -r skills/* ~/.gemini/antigravity-cli/skills/
```
Antigravity will automatically index these skills and invoke them whenever you prompt for UI design, color palettes, UX reviews, or design system architectures.

### 2. Claude Code, Cursor, Windsurf & Other AI Coding Assistants
You can use these skills directly in your project workspace by keeping the `skills/` folder at project root, or referencing individual skill files:
```text
"Review this dashboard according to skills/refactoring-ui/SKILL.md and verify navigation with skills/web-usability-krug/SKILL.md."
```

### 3. Prompting Example
```text
User: "Design an accessible, modern pricing card component in Tailwind CSS."
Agent: [Activates `refactoring-ui` and `color-interaction-albers`]
- Applies 8-pt spacing scale
- Enforces grayscale-first layout for visual weight
- Uses Albers' simultaneous contrast principles for call-to-action button prominence
- Verifies Krug's billboard scanability
```

---

## 🤖 Synthesis Engine & Quality Guarantee

* **Synthesized with Claude Fable 5.1:** Anthropic's premier frontier model for long-horizon autonomous workflows, complex synthesis, and precise instruction modeling.
* **Uncompromising Source Fidelity:** Every rule, number, and methodology directly references original chapters and author principles—no watered-down generic design advice.
* **Operational Format:** Tailored specifically for AI context windows, with clear trigger conditions, structured workflows, diagnostic procedures, and checklists.

---

## 👤 Author & Maintainer

* **Author:** Yusif Azizov ([@Really-y](https://github.com/Really-y))
* **Repository:** [Really-y/ai-ui-color-design-skills-with-books](https://github.com/Really-y/ai-ui-color-design-skills-with-books)
