# Examples and cases from *The Elements of User Experience* (2nd ed.)

Compressed, with the lesson each teaches. Chapter references in parentheses.

## Table of contents
1. Why UX matters (ch. 1)
2. The model and the schedule (ch. 2)
3. Strategy (ch. 3)
4. Scope (ch. 4)
5. Structure (ch. 5)
6. Skeleton (ch. 6)
7. Surface (ch. 7)
8. Applying the elements (ch. 8)

---

## 1. Why UX matters (ch. 1)

**"One of those days" chain.** Alarm clock reset overnight (a cat stepping on it could change the time;
a different button configuration would have prevented it); coffeemaker power button gives no feedback
(no light, sound or tactile resistance) so the user thinks it's on; the auto-brew feature was never
learned (display still blinking 12:00); gas pump gives no hint which way to swipe the card; register so
complex the clerk restarts transactions; a driver crashes because the radio volume knob can't be
identified by touch. Lesson: each piece of "bad luck" was a design choice; feedback, affordance and
control layout are UX decisions, and little things (a click) decide whether a customer returns.

**The chair vs the phone.** A chair you can't sit on isn't a chair: UX is built into the definition.
A telephone can be built infinitely many ways while still "placing calls": UX requirements are
independent of the definition, and every added feature is another place to fail. Lesson: complexity
is why UX design exists as a discipline.

**Conversion arithmetic.** 3 newsletter sign-ups from 36 visitors = 8.33% conversion. A shift of
0.1 percentage points in conversion can mean 10%+ revenue change. Lesson: conversion isolates the UX
contribution better than sales totals, which also reflect marketing.

## 2. The model and the schedule (ch. 2)

**Roof before foundation.** Two effort-over-time sketches: finishing each plane before starting the
next yields poor results; letting planes overlap but requiring each to *finish* after the one below
works. Lesson: the ripple rule is about finish order, not start order.

**Book covers.** An online bookstore wants cover images for every book. Can they be obtained?
Cataloged? Kept current? What if some can't be had? Lesson: content availability shapes the
experience as much as any element; ask early.

## 3. Strategy (ch. 3)

**Too general / too specific objectives.** "Make money" says nothing about how this product does it;
"provide a real-time text communications tool" is a solution that explains neither the organizational
nor the user benefit. Lesson: describe success conditions, not the path.

**Ad impressions trap.** Inserting navigation pages between home and content raises impressions, then
frustrated users stop returning and impressions sink below the starting point. Lesson: metrics
optimized against user needs reverse in the long run.

**Visits-per-registered-user chart.** Monthly visits per registered user plotted against a target line,
with the redesign launch marked. Lesson: a success metric needs a target, a timeline and a marker of
the design change it should affect.

**Stock-trading app.** Novices need a sequence of simple steps; experts need one unified, fast
interface; the same solution can't serve both. Options: pick one segment, or build two paths. Lesson:
opposed needs are a strategic fork, decided before design.

**Segment revision.** Researching college-educated women 25-34 may reveal 25-29 and 30-34 differ
enough to split, or that 18-24 is similar enough to merge. Lesson: segments exist only to capture
distinct needs.

**Janet and Frank.** Business-startup information site; audience 30-45, tech-comfortable, mixed
business experience. Janet, 42, accounting VP, married with two children, $180k household income,
15-20 hours/week online, "I don't have time... I need quick answers." Frank, 37, school-bus driver and
hobby woodworker, $60k, somewhat uncomfortable with technology, 8-10 hours/week online, "This stuff is
all new to me. I want a site that will explain everything." Lesson: two personas spanning the range of
needs, each with a quote that doubles as a design test.

**Customer-support site stakeholders.** Marketing communications, customer service and product
managers all have a say. Lesson: stakeholders are whoever owns an affected part of the organization,
formal or political.

## 4. Scope (ch. 4)

**Perpetual beta.** A Web application never launched; technology shaky, no user knowledge, but the real
block was refusing to write requirements because "we all sit in the same office" and the product
manager preferred inventing features. Result: an ever-changing mishmash with no schedule, milestones or
end. Lesson: without scope nobody can know when they're done.

**Support docs and spec sheets.** Listed as separate content features, written requirements showed
heavy overlap and that one group should own both. Lesson: mapping scope reveals connections.

**Version 1.0 / 1.1 timeline.** Requirements that don't fit the current schedule seed the next
milestone. Lesson: "not building" means "not building now".

**Six EVPs and a lawyer.** If every press release needs that approval chain, the CMS must support that
workflow. Lesson: content requirements create functional requirements.

**"Null input field exception".** An engineer's placeholder error shipped because nobody wrote error
messages as content requirements. Lesson: functional requirements create content requirements.

**Kite string.** "The system will not allow the user to purchase a kite without kite string" ->
"The system will direct the user to the kite string page if the user tries to buy a kite without
string." Lesson: positive requirements describe behavior that can be built and verified.

**Popular videos.** "The most popular videos will be highlighted" (popular by comments? likes?
highlighted how?) -> "Videos with the most views in the last week will appear at the top of the list."
Lesson: specificity prevents arguments during and after implementation.

**Hip and flashy.** "The site will have a hip, flashy style" (not falsifiable) -> "will meet the
hipness expectations of Wayne, the mail clerk" (falsifiable but arbitrary) -> "The look of the site
will conform to the company branding guidelines document" (objective; the VP of marketing can consult
Wayne, her teenage daughter or research to make the guidelines hip). Lesson: move taste out of the
requirement and into a referenced standard.

**1,000 simultaneous users.** "High level of performance" -> "designed to support at least 1,000
simultaneous users"; a system limited to three-digit user counts visibly fails it. Lesson: quantify.

**FAQs.** Stakeholders ask for FAQs; the format is a Q&A list, the purpose is ready access to commonly
needed information; most FAQs ignore "frequently". Lesson: specify purpose, then choose format.

**Thumbnails vs full-screen photos.** Knowing image dimensions in advance changes the design of the
vehicle for them. Lesson: rough content sizes belong in requirements.

**Kids and parents.** Information for children, for parents, and for both needs three presentations.
Lesson: record the audience per content piece.

**One-step order vs legacy databases.** Users want single-step submission; legacy databases can't take
all the data at once. Multi-step flow or database rework? Decided by strategic objectives. Lesson:
feature conflicts are resolved at strategy.

**Smelling products over the Web.** Technically impossible no matter how wanted. Lesson: feasibility
has a hard floor.

**Gaming social groups -> DVR.** A feature from an unrelated category inspires a requirement. Lesson:
non-competitors are a source too.

## 5. Structure (ch. 5)

**Cart vs catalog order form.** Container model: add/remove, "put in / take out", checkout. Order-form
model: an edit function replaces add/remove; "send in" the order. Both work; the cart is a convention
users bring from other stores. Lesson: pick the model users already hold unless you have a reason
and a model they'll understand.

**Slate as a magazine.** Front, back, page numbers, "turn the page" controls; the model didn't fit the
Web and was dropped. Lesson: whole-product metaphors from other media rarely survive.

**Southwest Airlines' service desk.** Home page was a picture of a counter with brochures and a
telephone; held up for years as a metaphor taken too literally; later replaced by a functional,
metaphor-light site. Lesson: analogies guide design, they don't dictate the interface.

**Automatic transmission.** Starter won't engage unless the transmission is disengaged, so the error of
starting in gear can't happen. Lesson: the best error handling makes the error impossible.

**Word's auto-corrections.** Features meant to fix errors get switched off so the user can stop
correcting the corrections. Lesson: automatic fixing can be worse than the error.

**Seven steps vs three.** A clear seven-step process beats a confusingly compressed three-step one.
Lesson: don't count clicks; check that each step follows naturally.

**Press releases.** Day-by-day paging works for a few months of releases; by topic becomes practical
after years. Lesson: organizing principles expire as content accumulates.

**Color vs size browsing.** Some users browse products by color, others by size; a matrix structure
serves both. Lesson: matrix axes map to distinct user needs.

**Cars by weight.** A consumer site ordered by vehicle weight is wrong (make/model/type is right); for
professionals shipping cars overseas, weight is exactly right and fuel economy irrelevant. Lesson: the
right facet depends on the audience; wrong facets are worse than none.

**Consumer / Business / Investor; North America / Europe / Africa; Baseball / Tennis / Hockey.** Top
levels organized by audience or geography (strategy-driven); news by chronology; next level by content
topic. Lesson: organizing principle changes with level.

**Volunteer fire departments article.** Metadata (author, date, piece type, product, product type,
customer industry, related topics such as municipal agencies and emergency services) lets the company
spin up an "emergency services" section instantly when that market appears. Lesson: rich, consistent
metadata buys structural flexibility.

**Smarter search.** Search for a disallowed term -> thesaurus maps to the preferred term -> metadata
lookup returns targeted results plus related topics, instead of zero hits. Lesson: vocabulary +
metadata upgrade "very dumb" search.

## 6. Skeleton (ch. 6)

**Windshield washers.** Friends driving Garrett's car washed the windshield when trying to turn on the
headlights because the controls broke convention. Lesson: broken conventions trigger wrong reflexes.

**Phone keypads.** 3x4 is the standard; variants (2x6, circular) cost maybe three seconds of pure
frustration per call. The phone layout spread to microwaves and remotes; the inverted "10-key" layout
rules calculators, keyboards, ATMs and registers; both are 3x4 so people cope, though one standard
would be best. Lesson: deviate only for clear benefit; small delays carry large frustration.

**Telephone icon.** Make a call? Check voicemail? Pay the bill? Lesson: metaphorical icons invite
multiple readings; some users always guess wrong.

**Phone-book icon vs coffee-shop chat.** A directory shown as a phone book reduces effort; a chat area
shown as a coffee shop obscures it. Lesson: keep a metaphor only when it lowers mental effort.

**"Show Me More Detail" checked by default.** If most users want detail, the default serves them
without reading the label; remembering last choices is better still but can be technically costly.
Lesson: defaults are a cheap way to serve the majority.

**Dropdown vs radio buttons (figure).** The dropdown hides important options; radios show all but take
space. Typing a category spares the database but burdens the user; with six categories, checkboxes
may be better. Lesson: every control choice is a trade-off between space, visibility and user load.

**Store hours at the entrance.** Rarely needed, but reassuring to know it's there; courtesy navigation
(contact, feedback, policies) works the same way. Lesson: courtesy nav is for convenience, not for
frequent tasks.

**Contact-form grouping.** A scrambled list (State, Job title, Telephone, Street, Name, Zip,
Organization, City, E-mail) reads badly; the conventional order (Name, Job title, Organization,
Street, City, State, Zip, Telephone, E-mail) reads fine; grouping into Personal / Address / Other
contact information is clearer still. A list like Power limit, Rotor size, Tank capacity, Transmission
type, Median angular velocity, Chassis style, Maximum output is harder because no convention exists.
Lesson: information design is micro-IA; group the way users think.

**Parking garage colors; airport signs.** Physical wayfinding devices; on screen, section color coding
reinforces (never replaces) other cues. Lesson: layer wayfinding cues.

**Wireframe figure.** Regions: logo, global nav, courtesy nav (top and bottom), wayfinding cues,
search (dropdown, text field, button), header graphic, local nav, supplementary nav, body text,
partner content; annotated lightly. Lesson: a wireframe captures every skeleton decision in one
reference document.

**Pencil sketches with sticky notes.** Among the most successful wireframes Garrett used, for a
designer and programmer sitting side by side; a distributed programming team needs something formal.
Lesson: scale documentation to team distance.

## 7. Surface (ch. 7)

**Car chimes and TiVo sounds.** Beeps that say headlights on, seat belt off, key in ignition; TiVo's
sounds give personality. Lesson: sound informs and brands.

**Comic fonts for a technical brand.** A technical, authoritative identity is undermined by comic-book
type and bright pastels. Lesson: visual choices are strategy decisions.

**Squint test.** Blur your eyes or stand across the room to find the dominant element; ask testers to
call out elements in attention order. Lesson: cheap "follow the eye" checks are usually enough.

**Four layouts figure.** Visually neutral (nothing stands out); contrast guiding the eye around the
page; contrast focusing on a few key elements; overused contrast producing clutter. Lesson: contrast
is a dial with a sweet spot.

**Red error text.** Error messages that blend in get missed; a different color or bold graphic fixes
it. Lesson: errors are a contrast problem on the surface plane.

**Big round red STOP button.** Works on the checkout page, may fail on the crowded customization page.
Lesson: design elements once, then verify in every context.

**Coca-Cola, UPS, Kodak.** Red, brown, yellow used for years become identity; each sits in a broader
complementary palette. Orbitz uses a limited palette to differentiate features. Lesson: a few
consistent, distinguishable colors beat many.

**Apple, Volkswagen, London Underground, Martha Stewart.** Custom typefaces as identity; optional. Body
text in Helvetica/Times-style simplicity; personality reserved for headings and labels. Lesson: type
serves readability first, identity second.

**Wireframe vs comp figure.** The comp rearranges the page but keeps the branding area, global nav,
courtesy nav, featured items, supplementary nav, top national/local stories with the same relative
importance and grouping. Lesson: comps honor the wireframe's priorities, not its pixels.

**Organizational amnesia.** Reasons fade; people leave with the know-how; without a current style guide
the organization forgets why things are done. Lesson: the style guide is institutional memory.

## 8. Applying the elements (ch. 8)

**Big purple button.** Is the problem its size and color (surface), its position (skeleton), or that
the function doesn't do what users expect (structure)? Lesson: locate the plane before fixing.

**Order history and billing in separate databases.** Keeping them separate in the UX because the
database does is design by default. Lesson: user-facing structure needn't mirror technical structure.

**Orange and dropdowns.** Orange dominates because an SVP likes it; every nav element is a dropdown
because the head engineer prefers them. Lesson: design by fiat replaces objectives with preference.

**Navigation bar: color or wording?** A prototype test that doesn't isolate the question can't tell.
Lesson: know which element you're testing and strip distractions.

**"User acceptance testing".** Testing at the very end asks only "can they accept it?", after
assumptions are buried under interface layers and money is gone. Lesson: evaluate throughout, not at
the finish line.

**Marathon vs sprint.** Teams in permanent emergency sprint every project; product development is a
marathon with pushes and pull-backs, requiring constant monitoring and pacing. Lesson: plan the
rhythm, not just the deadline.

**Beautiful but unusable.** Sites that focused on visual design to the exclusion of lower planes
bankrupted start-ups; conversely, clutter and clashing colors can hide excellent navigation and
interaction work. Lesson: every plane can sink the others.
