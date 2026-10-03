# AI UI & Color Design Skills With Books 🎨📚

> **Bütün klassik UI/UX, rəng və dizayn kitabları Claude Fable 5.1 ilə oxunub, analiz edilib və operativ AI agent bacarıqlarına (skills) çevrilmişdir.**  
> *Every foundational UI/UX, color, and design book has been read, synthesized, and transformed into operational AI agent skills powered by **Claude Fable 5.1**.*

---

## 📖 Layihə Haqqında / About

Bu repozitoriya müasir rəqəmsal məhsul dizaynının, istifadəçi təcrübəsinin (UX), vizual iyerarxiyanın və dizayn sistemlərinin qızıl standartı sayılan ən mühüm kitablarının bilik bazasını özündə cəmləşdirir.

Bütün kitablar **Claude Fable 5.1** tərəfindən səhifə-səhifə oxunmuş, metodoloji çərçivələrə ayrılmış və AI agentlərinin (məsələn: **Antigravity**, **Claude Code**, **Cursor**, **Windsurf** və s.) birbaşa layihələrdə tətbiq edə biləcəyi `SKILL.md` və köməkçi referans pleybuklarına (`references/`) çevrilmişdir.

---

## 📚 Kitablar və Hazırlanmış Bacarıqlar (Skills)

| Kitab və Müəllif | Bacarıq Qovluğu | Təsvir və Əsas Fokus |
| :--- | :--- | :--- |
| **Refactoring UI**<br>*Adam Wathan & Steve Schoger* | [`skills/refactoring-ui`](./skills/refactoring-ui) | Tərtibatçılar üçün vizual dizayn. 8-point grid, tipoqrafik iyerarxiya, rəng şkalaları, dərinlik/kölgələr və praktiki interfeys detalları. |
| **The Elements of User Experience**<br>*Jesse James Garrett* | [`skills/ux-five-planes`](./skills/ux-five-planes) | 5 UX Təbəqəsi: **Strategy → Scope → Structure → Skeleton → Surface**. Məhsul strategiyasından son vizual səthə qədər addım-addım planlama və audit. |
| **Don't Make Me Think, Revisited**<br>*Steve Krug* | [`skills/web-usability-krug`](./skills/web-usability-krug) | Veb və mobil istifadəyəyararlılıq (Usability). Sürətli skan edilə bilən səhifələr, Trunk Test, naviqasiya aydınlığı və "az xərclə maksimum fayda" testləri. |
| **The Design of Everyday Things**<br>*Don Norman* | [`skills/design-of-everyday-things`](./skills/design-of-everyday-things) | İnsan mərkəzli dizayn (HCD). Affordances, signifiers, mappings, feedback, 7 fəaliyyət mərhələsi və səhvlərin profilaktikası/idarə edilməsi. |
| **Interaction of Color**<br>*Josef Albers* | [`skills/color-interaction-albers`](./skills/color-interaction-albers) | Rənglərin qarşılıqlı təsiri, simultan kontrast, işıqlıq və doyğunluq aldanışları, UI interfeyslərində harmoniya və oxunaqlılıq. |
| **Atomic Design**<br>*Brad Frost* | [`skills/atomic-design`](./skills/atomic-design) | Atomik dizayn fəlsəfəsi: Atoms → Molecules → Organisms → Templates → Pages. Pattern Lab, JSON ilə strukturun ayrılması və komponent sistemləri. |
| **Atomic Design Systems**<br>*Brad Frost Methodologies* | [`skills/atomic-design-systems`](./skills/atomic-design-systems) | İnterfeys inventarlaşdırılması (Interface Inventory), komponentlərin təsnifatı (Classify Component) və dizayn sisteminin idarəetmə prinsipləri. |

---

## 🛠️ Qovluq Strukturu / Directory Structure

Hər bir bacarıq müstəqil şəkildə strukturlaşdırılıb və aşağıdakı elementləri ehtiva edir:

```bash
skills/
├── atomic-design/
│   ├── SKILL.md                          # Əsas bacarıq qaydaları və triggerlər
│   └── references/                       # Chapter map, glossary, methodology, patternlab, principles
├── atomic-design-systems/
│   └── references/                       # Classify component, interface inventory, principles
├── color-interaction-albers/
│   ├── SKILL.md                          # Josef Albers rəng nəzəriyyəsi və UI qaydaları
│   └── references/                       # Apply to UI, examples, principles, critique
├── design-of-everyday-things/
│   ├── SKILL.md                          # Don Norman-ın koqnitiv dizayn metodologiyası
│   └── references/                       # Diagnose interaction, design for error, playbook
├── refactoring-ui/
│   ├── SKILL.md                          # Steve Schoger və Adam Wathan-ın dizayn qaydaları
│   └── references/                       # Scales and systems, audit checklist, three-phase loop
├── ux-five-planes/
│   ├── SKILL.md                          # Jesse James Garrett-in 5 mərhələli UX arxitekturası
│   └── references/                       # Planes checklist, playbook, glossary
└── web-usability-krug/
    ├── SKILL.md                          # Steve Krug-un usability qanunları
    └── references/                       # Trunk test, usability test kit, playbook, principles
```

---

## 🚀 Bacarıqların İstifadəsi / How to Use

### 1. Antigravity CLI / Google Agentic Environment
Bu skildən Antigravity daxilində qlobal və ya layihə səviyyəsində istifadə etmək üçün:
```bash
# Qlobal skiller qovluğuna kopyalamaq
mkdir -p ~/.gemini/antigravity-cli/skills
cp -r skills/* ~/.gemini/antigravity-cli/skills/

# Və ya birbaşa cari iş sahənizdə saxlamaq
```

### 2. Claude Code və digər AI Agentlər
Agentinizə dizayn auditləri və ya komponent sistemləri qurarkən müvafiq `SKILL.md` fayllarını sistem təlimatlarına daxil edərək və ya kontekstə əlavə edərək göstəriş verə bilərsiniz:
> *"Audit this dashboard following `skills/refactoring-ui/SKILL.md` and check the usability with `skills/web-usability-krug/SKILL.md`."*

---

## 🤖 Model & Synthesis Qeydləri

- **Metodologiya:** Kitabların orijinal məzmununa xələl gətirilmədən, hər bir müəllifin orijinal fəlsəfəsi, terminologiyası və təcrübi addımları dəqiqliklə saxlanılmışdır.
- **Sintez Mühərriki:** **Claude Fable 5.1** (Anthropic-in mürəkkəb bilik sintezi və proqramlaşdırma üzrə flaqman modeli).
- **Müəllif & Repozitoriya:** Yusif Əzizov ([@Really-y](https://github.com/Really-y)) | [ai-ui-color-design-skills-with-books](https://github.com/Really-y/ai-ui-color-design-skills-with-books)
