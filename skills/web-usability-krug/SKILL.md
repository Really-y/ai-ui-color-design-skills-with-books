---
name: web-usability-krug
description: Steve Krug's "Don't Make Me Think, Revisited" turned into an operational web & mobile usability skill. Use it to audit or design pages, screens, navigation, home pages, forms, copy and mobile apps for at-a-glance clarity; to plan and run do-it-yourself usability tests (3 users, one morning a month, script, debrief, "fix the most serious first" triage); to settle design "religious debates" with evidence instead of opinion; to run a goodwill/courtesy audit, an accessibility quick-start, or a "trunk test" page audit; and to get managers to care about usability. Trigger on requests like "review this UI / landing page / home page / checkout / onboarding", "is this clear or confusing", "why do users get lost", "too many clicks?", "do we need a tagline", "trim this copy / these instructions", "plan a usability test", "how many test users", "write a test script", "what should we fix first", "focus group or usability test", "convince my boss about UX", "accessibility quick wins", "mobile app is hard to learn" — even when the user never names Krug or the book.
---

# Web usability the Krug way

This skill gives you Steve Krug's working method for making web sites, web apps and mobile apps usable: a thing is usable when "a person of average (or even below average) ability and experience can figure out how to use the thing to accomplish something without it being more trouble than it's worth" (Introduction). The core thesis in operational terms: real people do not read pages, weigh options or learn how things work — they scan, pick the first reasonable option (satisfice) and muddle through (ch. 2). So every page must work at a glance, like a billboard seen at 60 mph (ch. 3). Your job on any page is to remove the question marks over the user's head (ch. 1), and the only reliable way to know whether you succeeded is to watch a few real people try to use it, early and often, and fix the worst problems first (ch. 8–9). Clarity is half of usability; the other half is behaving like a mensch — being considerate of the user (ch. 11) — and being accessible (ch. 12).

## Workflow

1. **Frame the task.** Is the artifact a page/screen, a navigation system, a Home page, copy, a form/choice, a mobile app, a test plan, a team argument, or a management problem? Pick the matching playbook section (table below).
2. **Audit at a glance before you audit in detail.** Squint. Ask the ch. 1 questions a user shouldn't have to think about: Where am I? Where should I begin? Where did they put ___? What are the most important things on this page? Why did they call it that? Is that an ad or part of the site? Run the trunk test on any interior page (`references/trunk-test.md`).
3. **Diagnose with Krug's categories.** Every finding maps to one of: makes me think (names, clickability, choices), fights scanning (hierarchy, areas, noise, text formatting), weak scent/hard choices, needless words, broken navigation conventions, missing big picture on Home, goodwill-draining behavior, or inaccessible structure. Attribute it; say why it costs the user.
4. **Prescribe the cheapest fix that removes the question mark.** Prefer taking something away over adding explanations or instructions (ch. 9 debrief tip). Follow conventions unless you have a clearly better idea (ch. 3). Make cues "twice as prominent" as a designer thinks is tasteful (ch. 6).
5. **Replace opinion with observation.** When the question is "do people like X?", reframe to "does this X, with these items and this wording, in this context, on this page, work for the people likely to use this site?" and propose a test (ch. 8). Plan it with `references/usability-test-kit.md`.
6. **Triage.** List observed problems, pick the ten most serious, rank 1–10, assign the least-you-can-do fix for the next month, then stop (ch. 9).

## Core rules (with the book's numbers)

1. Krug's First Law: **Don't make me think.** Each page should be self-evident; if it can't be, make it self-explanatory ("a little thought — but only a little") (ch. 1).
2. The neighbor test: someone with no interest in your subject who barely knows the Back button should look at the Home page and say "Oh, it's a ____." (ch. 1).
3. Names: skew tradeoffs further toward "obvious to everybody" than you think; cute, marketing-driven, company-specific and technical names make people think ("Jobs" beats "Job-o-Rama") (ch. 1).
4. Nobody should spend a millisecond wondering whether something is clickable. One color for all text links; never the same color for links and non-clickable headings (ch. 1, 3).
5. Design for scanning: users read only words matching their task, their interests, or hardwired triggers ("Free", "Sale", their name) (ch. 2).
6. Users satisfice — they click the first reasonable option because the Back button is cheap. Expect it; make the first reasonable option the right one (ch. 2).
7. Innovate only when you know you have a better idea; otherwise use the convention. A replacement must be either as clear as the convention (no learning curve) or add enough value to justify a small one (ch. 3).
8. **Clarity trumps consistency**: if a slight inconsistency makes something significantly clearer, choose clarity (ch. 3).
9. Visual hierarchy has three traits: importance = prominence; logical relation = visual relation; nesting shows what's part of what. A flawed hierarchy reads like a badly built sentence (ch. 3).
10. Break pages into clearly defined areas so users can point and say "things I can do here", "navigation", "stuff they're selling me" ($25,000 Pyramid test) (ch. 3).
11. Treat everything as visual noise, "presumed guilty until proven innocent"; the three noises are shouting, disorganization (no grid) and clutter (ch. 3).
12. Format text for scanning: more headings than you think (and don't let them float — closer to the text they introduce), short paragraphs (one sentence is fine), bulleted lists with a little space between items, bold key terms sparingly (ch. 3, 13).
13. Krug's Second Law: **It doesn't matter how many clicks, as long as each click is a mindless, unambiguous choice.** Rule of thumb: three mindless clicks equal one click that requires thought (ch. 4).
14. When a hard choice is unavoidable, give guidance that is brief, timely and unavoidable (tips next to fields, "What's this?", London's "LOOK RIGHT") (ch. 4).
15. Krug's Third Law: **Get rid of half the words on each page, then get rid of half of what's left.** Happy talk ("Welcome to...", "world-class solutions") and instructions must die; a 103-word survey intro became 34 words (ch. 5).
16. Navigation is the site: it tells you what's here, how to use the site, and whether the builders know what they're doing (ch. 6).
17. Persistent navigation on every page carries Site ID, Sections, Utilities, Search and a way Home; only 4–5 utilities fit, the rest go in the footer. Forms are the one exception — strip to Site ID, Home and form-helping utilities (ch. 6).
18. Search: a box, a button, the word "Search" (or the magnifying glass). No "Find"/"Quick Search", no "type a keyword" instructions, no scope options up front — offer scoping on the results page (ch. 6).
19. Every page needs a name: framing the page's unique content, usually the largest text on the page, and matching the words the user clicked (the implicit social contract) (ch. 6).
20. "You are here" markers are usually too subtle; use at least two visual distinctions (e.g., color + bold). If a cue sticks out like a sore thumb to a designer, make it twice as prominent (ch. 6).
21. Breadcrumbs: at the top, `>` between levels, last item bold and not a link; most useful on large, deep sites (ch. 6).
22. Tabs: active tab must be a contrasting color and physically connect to the content below, so it "pops" in front (ch. 6).
23. Design sample pages for every level of the hierarchy before arguing about colors; lower-level nav is where most sites break down (ch. 6).
24. Trunk test: dropped blindfolded on a random page, you must instantly find Site ID, page name, sections, local navigation, "you are here", and search (ch. 6).
25. The Home page's first casualty is the big picture. It must answer at a glance what this is, what I can do here, what they have here, and why I should be here and not elsewhere — then the fifth question: where do I start (search / browse / best stuff)? (ch. 7).
26. Tagline next to the Site ID, 6–8 words, clear, differentiated ("no one else in the world could use it"), not a motto, not a mission statement. Test it with outsiders: the main point is the one thing insiders never notice is missing (ch. 7).
27. Guard the Home page against the tragedy of the commons: each new promo gains one stakeholder and costs everyone (ch. 7).
28. There is no Average User; all web use is idiosyncratic. Don't ask "do people like pull-downs?" — build it and watch people use it (ch. 8).
29. Focus groups are not usability tests: groups talking about opinions (planning stage) vs. one person at a time trying to use the thing (whole project) (ch. 9).
30. Testing one user is 100% better than none; one user early beats 50 near the end (ch. 9).
31. Cadence: one morning a month, three participants, debrief over lunch; pick a fixed day (e.g., third Thursday). Agile: e.g., two users every two weeks (ch. 9).
32. Recruit loosely and grade on a curve; always include some people outside the target audience (ch. 9).
33. Facilitator's prompt is "What are you thinking?"; when asked for help: "What would you do if I wasn't here?" Save probing questions for the end (ch. 9).
34. "You can find more problems in half a day than you can fix in a month" — so focus ruthlessly on fixing the most serious problems first; a tweak that drops a problem out of "serious" is enough (ch. 9).
35. Ignore "kayak" problems (user goes astray, notices quickly, recovers unaided, isn't fazed); distrust participants' feature requests (ch. 9).
36. Mobile: same principles, people read even less. Most serious problems come from bad tradeoffs; "managing real estate challenges shouldn't be done at the cost of usability." Keep affordances visible; nothing can depend on hover; compensate for flat design with the remaining dimensions; speed matters more (ch. 10).
37. Mobile sites: allow zooming, deep-link to the content (not the mobile Home), and always link to the full site (ch. 10).
38. Users arrive with a reservoir of goodwill that is idiosyncratic, situational, refillable, and can be emptied by one mistake (e.g., a huge registration form). Don't hide prices, shipping or support numbers; never punish data formatting; ask only for what you need (ch. 11).
39. Accessibility step one is fixing what confuses everyone; then alt text, correct heading levels, `<label>`s, "Skip to Main Content", keyboard access, strong contrast, accessible templates (ch. 12).
40. Definitive always/nevers: no small low-contrast type; no labels inside form fields (with narrow exceptions); keep visited vs. unvisited link colors different; never float headings (ch. 13).

## When to read which reference

| Task | Read |
|---|---|
| Any page/screen review; checklist-driven audit | `references/trunk-test.md` (billboard, navigation, Home, mobile, courtesy checklists) then `references/playbook.md` §1 |
| Understand/explain a principle, definition or the reasoning behind a rule | `references/principles.md` (grouped by theme, each with why/how/pitfalls) |
| Design or fix navigation, breadcrumbs, tabs, search, page names | `references/playbook.md` §2; `references/principles.md` "Navigation" |
| Home page / landing page / tagline / "what is this site" | `references/playbook.md` §3; `references/principles.md` "Home page" |
| Write or cut copy, instructions, labels, FAQs | `references/playbook.md` §4; `references/examples.md` (survey 103→34 words) |
| Forms, choices, decision points, "which one am I?" | `references/playbook.md` §5 |
| Convention vs. innovation, consistency arguments, flat design | `references/playbook.md` §6; `references/examples.md` |
| Team argument about what users like | `references/playbook.md` §7 (religious debates antidote) |
| Plan, recruit, script, facilitate, observe, debrief and triage a usability test (desktop or mobile) | `references/usability-test-kit.md` |
| Mobile app/site review (learnability, memorability, affordances, speed, responsive) | `references/playbook.md` §8; `references/principles.md` "Mobile" |
| Courtesy / goodwill / trust audit; FAQ and support pages | `references/playbook.md` §9; `references/trunk-test.md` courtesy checklist |
| Accessibility quick start | `references/playbook.md` §10 |
| Convincing a boss, building a usability practice, dark patterns requests | `references/playbook.md` §11–12 |
| Concrete before/after cases to cite or imitate | `references/examples.md` |
| Rebut "we don't need to explain the site" / "we can't test" objections; explain DIY vs traditional testing to a manager | `references/figures.md` (the book's tables, transcribed) |
| Verify a claim against the book | `references/chapter-map.md` |

## Anti-patterns the author calls out

- Designing for an imagined attentive reader ("great literature") when the user sees a billboard at 60 mph (ch. 2).
- Reinventing conventions (custom scrollbars) because "we were hired to do something new"; awards are never for "best use of conventions" (ch. 3).
- Winning arguments with "it wouldn't be consistent" when a small inconsistency would be clearer (ch. 3).
- Shouting: everything bold, bright, animated, exclamation-pointed — a failure to decide what matters (ch. 3).
- Click-count rules ("never more than 3 clicks") instead of asking how hard each click is (ch. 4).
- Top-level choices users can't map themselves onto ("Home office / Small business / Enterprise"; "Stamped mail / Metered mail") (ch. 4).
- Happy talk, welcome paragraphs, mission statements as Welcome blurbs, and wordy instructions nobody reads (ch. 5, 7).
- Highlighting the current item in the nav and calling that the page name; page names that don't match the link text (ch. 6).
- Subtle "you are here" cues; search boxes labeled "Find" with scope options and "type a keyword" (ch. 6).
- Designing the Home page and two levels, then letting third-level navigation become ad hoc (ch. 6).
- Promoting everything on the Home page ("I see stakeholders"); obscuring entry points with promos yelling "Start here!" (ch. 7).
- Debating what the Average User likes; using focus groups when you need a usability test; testing to settle aesthetics ("which drapes") while the room has no windows (ch. 8–9).
- Big-deal testing: narrow recruiting profiles, labs, 50 users at the end, "we'll test when the beta is ready" (ch. 9).
- Fixing low-hanging fruit instead of the one serious problem; adding explanations instead of removing what obscures (ch. 9).
- Mobile: interpreting Mobile First as "only features for people on the move"; hover-dependent UI; flat design that erases affordances; loading full-size assets on 3G; sending deep links to the mobile Home page (ch. 10).
- Hiding prices, shipping and phone numbers; rejecting credit-card numbers with spaces; "Your call is important to us"; QWWPWAs (Questions We Wish People Would Ask) posing as FAQs (ch. 11).
- Treating accessibility as a validator pass or an "initiative" with task forces, rather than clarity first plus a short list of fixes (ch. 12).
- Preaching usability to "the unwashed masses" instead of getting the boss to watch one live test (ch. 13).
- Using usability testing to measure desirability or to engineer manipulation (pre-checked boxes, fake "Start Download" buttons): "it's not part of your job" (ch. 13).
