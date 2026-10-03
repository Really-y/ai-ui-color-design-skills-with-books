# Usability test kit — Krug's do-it-yourself method (ch. 9, with ch. 10 mobile logistics and ch. 13 tactics)

Everything needed to plan, run, observe, debrief and triage a round of do-it-yourself usability testing. Script wording is quoted from the book's sample session; Krug recommends reading the lines exactly as written and offers the full script (web and app versions), forms and checklists at rocketsurgerymadeeasy.com.

## Contents
1. What this method is (and isn't)
2. Program design: cadence, numbers, cost
3. Recruiting
4. Setup: rooms, equipment, roles
5. What to test and when; writing tasks
6. The one-hour session structure
7. The script (facilitator lines)
8. Facilitation rules
9. Mobile testing logistics
10. Observer protocol
11. The debrief and triage method
12. Deciding what to fix — rules of thumb
13. Alternatives: remote and unmoderated
14. Checklists

---

## 1. What this method is (and isn't)

- **Usability test**: watch one person at a time try to use something (site, prototype, sketches, app) to do typical tasks, so you can detect and fix what confuses or frustrates them. The point is *watching people use things*, not listening to them talk about them.
- **Not a focus group**: 5–10 people around a table discussing opinions, experiences and concepts — useful for whether the idea makes sense and the value proposition is attractive, how people currently solve the problem, feelings about you and competitors; belongs in planning, before building. Not for whether the site works.
- **Qualitative, not proof.** No statistics, no rigid protocol: give tasks, observe, learn. Output is actionable insight. "You can find more problems in half a day than you can fix in a month," so finding every problem is not the goal — fixing the worst ones is.
- **Participants**, not "test subjects": "we're testing the site, not you."
- If you can afford a professional, hire one; they'll do it better. If not, this.

## 2. Program design: cadence, numbers, cost

| Decision | Krug's answer | Why |
|---|---|---|
| How often | One morning a month | Simple enough that you keep doing it; three users yield a month of fixes; frees you from deciding when |
| When | A fixed day (e.g., the third Thursday), never a milestone ("when the beta is ready") | Milestones slip and testing slips with them; a predictable day gets observers to attend; there's always something to test |
| Agile variant | e.g., two users every two weeks | The principle is a fixed schedule |
| How many participants per round | Three | Enough to hit many of the most significant problems for the tasks; more rounds beat more users per round |
| Session length | One hour (about 35 minutes of tasks) | Plus roughly an hour of travel for the participant |
| Incentive | $50–$100 for average Web users; several hundred for busy highly paid professionals (e.g., cardiologists); pay a bit above the going rate | Shows you value their time; improves show-up rate |
| Budget history | Lab studies $20,000–$50,000; Nielsen's discount testing $5,000–$10,000 per round; DIY: essentially snacks and incentives | Testing has to be cheap to happen often |
| Earliest start | Before design: test competitors' sites with 3 participants | Learn what works without building anything |

## 3. Recruiting

- **Recruit loosely and grade on a curve.** Aim for people like your users but don't get hung up; loosen requirements, then for each observed problem ask: "Would our users have that problem, or was it only a problem because they didn't know what our users know?"
- If the site needs domain knowledge, recruit *some* participants with it — not all; many serious problems hit everyone.
- Always include some participants outside the target audience: designing only for insiders fails some insiders too; experts muddle through at a higher level; experts aren't insulted by true clarity.
- Avoid over-specified profiles ("male accountants 25–30 with 1–3 years' computer experience who recently bought expensive shoes") unless you have the time/money and it won't reduce how much testing you do.
- Sources: user groups, trade shows, Craigslist, Facebook, Twitter, customer forums, a pop-up on your site, friends and neighbors. Resource: Nielsen Norman Group's free report "How to Recruit Participants for Usability Studies" (2003; add ~20% inflation to dollar figures).
- Remote testing widens the pool from "people near the office" to "almost anyone" (see §13).

## 4. Setup: rooms, equipment, roles

**Test room**: quiet, uninterrupted (office or conference room); table or desk; two chairs; computer with Internet, mouse, keyboard, microphone; screen-sharing software (e.g., GoToMeeting, WebEx) so observers watch from another room; screen-recording software (e.g., Camtasia) capturing screen plus facilitator/participant audio (you may never watch it, but it's there for checking details or short presentation clips). Open the browser to Google (nothing distracting) before the participant arrives.

**Observation room**: conference room; computer with Internet and the screen-share; large monitor or projector; external speakers; the best snacks you can buy (chocolate croissants) to lure people in.

**Roles**
- *Facilitator*: sits with the participant, leads the session, keeps them comfortable and focused, keeps them thinking aloud. Almost anyone can do it with courage and practice; if choosing someone, pick patient, calm, empathetic, a good listener — not "the office crank." Role is good listener, not expert; admit ignorance freely.
- *Observers*: as many as possible — team members, stakeholders, managers, executives. Watching is transformative: people "get it" that users aren't like them. Each writes down the three most serious problems after each session (§10).
- *Participant*: one at a time.

## 5. What to test and when; writing tasks

**When**: never too early. Before designing, test one or two competitive sites (actual competitors or sites with similar style/organization/features). Redesigning? Test the existing site first to learn what's broken and what works so you don't break it. Then test everything the team produces: rough sketches → wireframes → page comps → prototypes → live pages.

**Tasks**
1. If all you have is a sketch: the task is "look at it and tell me what you think it is."
2. Otherwise list what people need to be able to do with the thing (login prototype: create an account; log in with existing credentials; retrieve a forgotten password; retrieve a forgotten username; change a security-question answer).
3. Choose enough tasks for ~35 minutes; some participants finish faster, so have spares.
4. Word each task so the participant knows exactly what to do, and include information they'd need but don't have (demo credentials). Example: "You have an existing account with the username delphi21 and the password correcthorsebatterystaple. You've always used the same answers to security questions on every site, and you just read that this is a bad idea. Change your answer for this account."
5. Let participants choose details where possible: "Find a book you want to buy, or a book you bought recently" rather than "Find a cookbook for under $14" — more emotional investment and real knowledge.
6. Prepare any probing questions the team wants asked at the end (e.g., "What did you make of the numbered pictures at the top?").

## 6. The one-hour session structure

| Segment | Time | Purpose |
|---|---|---|
| Welcome | 4 min | Explain how the test works so they know what to expect; get recording permission signed |
| The questions | 2 min | A few background questions; puts them at ease; gauges computer/Web savvy |
| Home page tour | 3 min | They look at the Home page and say what they make of it — reveals how understandable Home is and their domain knowledge |
| The tasks | 35 min | The heart: watch them attempt tasks while thinking aloud |
| Probing | 5 min | Ask about anything that happened; relay observers' questions |
| Wrapping up | 5 min | Thank, pay, show them out |

Between sessions: break for observers to write their three most serious problems. Three sessions in a morning; debrief over lunch.

## 7. The script (facilitator lines)

Read it; say you're reading it so nothing is missed. (Sample session with "Janice," ch. 9.)

**Introduction**
> Hi, ___. My name is ___, and I'm going to be walking you through this session. Before we begin, I have some information for you, and I'm going to read it to make sure I cover everything.
> You probably already have a good idea of why we've asked you to come here today, but let me go over it again briefly. We're testing a Web site that we're working on so we can see what it's like for people to use it. The session should take about an hour.
> I want to make it clear right away that we're testing the site, not you. You can't do anything wrong here. In fact, this is probably the one place today where you don't have to worry about making mistakes.
> We want to hear exactly what you think, so please don't worry that you're going to hurt our feelings. We want to improve it, so we need to know honestly what you think.
> As we go along, I'm going to ask you to think out loud, to tell me what's going through your mind. This will help us.
> If you have questions, just ask. I may not be able to answer them right away, since we're interested in how people do when they don't have someone sitting next to them to help, but I will try to answer any questions you still have when we're done.
> And if you need to take a break at any point, just let me know.
> You may have noticed the microphone. With your permission, we're going to record what happens on the screen and what you say. The recording will be used only to help us figure out how to improve the site, and it won't be seen by anyone except the people working on the project. It also helps me, because I don't have to take as many notes.
> Also, there are a few people from the Web design team observing the session in another room. (They can't see us, just the screen.)
> If you would, I'm going to ask you to sign a simple permission form for us. It just says that we have your permission to record you, but that it will only be seen by the people working on the project.
> Do you have any questions before we begin?

Why these lines: saying up front that you may not answer questions makes it not-rude later; "testing the site, not you" and "can't hurt our feelings" unlock honesty; recording consent is signed, not assumed.

**Background questions** (2 minutes; accuracy doesn't matter — the point is to get them talking, show you listen, and gauge what kind of user they are; digress briefly if interesting)
> Before we look at the site, I'd like to ask you just a few quick questions. First, what's your occupation? What do you do all day?
> Roughly how many hours a week would you say you spend using the Internet, including Web browsing and email? Just a ballpark estimate.
> What's the split between email and browsing — a rough percentage?
> What kinds of sites are you looking at when you browse the Web?
> Do you have any favorite Web sites?
> OK, great. We're done with the questions, and we can start looking at things.

**Home page tour** (open a tab with the site; hand over the mouse)
> First, I'm just going to ask you to look at this page and tell me what you make of it: what strikes you about it, whose site you think it is, what you can do here, and what it's for. Just look around and do a little narrative.
> You can scroll if you want to, but don't click on anything yet.

Follow-ups as needed: "If you had to take a guess, what do you think it might be?" — "OK. Now, if you were at home, what would you click on first?" Don't get excited by individual aesthetic reactions (the next participant may hate the orange).

**The tasks**
> OK, now we're going to try doing some specific tasks.
> And again, as much as possible, it will help us if you can try to think out loud as you go along.

Where possible let them pick the task details ("Can you think of some service that you need that you could use this site to get help with?" ... "So if you were going to look for somebody to build your deck, what would you do first?"). Then hand over the written task. Before they act on an uncertain choice: "Well, which one do you think you'd click on?" ... "Why don't you go ahead and do it?"

Let each task run until (a) they finish, (b) they get really frustrated, or (c) you're not learning anything new by watching them muddle. Three or four more tasks, not more than ~45 minutes in total.

**Probing**
> Now that we're done with the tasks, I have a few questions.
> What about [element]? What did you make of it?
> Any reason why you didn't pay much attention to it?

Ask here about anything surprising that happened and about elements the designers assumed everyone would use. Relay observers' questions.

**Wrap-up**: thank them, pay them, show them to the door.

## 8. Facilitation rules

- Prompt silence with: **"What are you thinking?"** Variants: "What are you looking at?" "What are you doing now?"
- Do not lead. No leading questions, no hints, no help — unless hopelessly stuck or extremely frustrated.
- If they ask for help: **"What would you do if I wasn't here?"**
- Keep quiet most of the time; save all "why" questions for probing at the end to avoid biasing behavior.
- Keep them comfortable and on task; keep them talking.
- Admit you don't know things; you're a listener, not an expert.
- Ignore comments about colors and looks unless three of four participants say something like "puke" (ch. 11).
- Treat "I'd like it if it could do X" with suspicion; during probing ask them to describe how it would work — they usually conclude they wouldn't use it (ch. 9).

## 9. Mobile testing logistics (ch. 10)

The process is identical (tasks, think-aloud, quiet facilitator, probing at the end, stakeholders observing). Only logistics differ, because robust mobile screen-sharing/recording apps weren't available (OS background-process limits; device horsepower).

Questions to settle: own devices or yours? held naturally or on a table/stand? what must observers see (screen only, or screen plus fingers/gestures)? how is it displayed in the observation room? how is it recorded?

Krug's recommendations:
1. **Camera pointed at the screen, not mirroring.** Mirroring (AirPlay, cables) shows the screen but not taps and gestures — like watching a player piano. Seeing hand + screen is far easier to follow.
2. **Attach the camera to the device** so the participant can hold it naturally; restricting movement only exists to keep a fixed camera aimed. A device-mounted camera keeps the screen in view and in focus.
3. **No face camera.** It's a distraction; tone of voice conveys feeling; a second camera complicates everything. (If the boss insists, show faces.)

"Brundlefly" rig: a lightweight webcam on a book-light clip/gooseneck with a padded clamp (no Velcro or tape), ~$30 in parts, ~1 hour to build, built-in mic, tiny and out of the participant's line of sight; tethered by a long USB extension. Setup: webcam → facilitator's laptop via USB; view it in AmCap (PC) or QuickTime Player (Mac); share the laptop screen to observers (GoToMeeting/WebEx); run the screen recorder (Camtasia) on the observation-room computer to spare the facilitator's laptop.

## 10. Observer protocol

- Watch from the observation room; don't interrupt the session.
- Take as many notes as you like, but in the break after **each** session write down the **three most serious usability problems** you observed in that session (Krug provides a form). Over three sessions, nine items per observer.
- Send probing questions to the facilitator before the probing segment.
- Come to the debrief with your list.

## 11. The debrief and triage method

Hold it as soon as possible — over lunch right after the sessions, while fresh. Order the really good pizza to encourage attendance. Goal: decide what to fix before the next round. Maxim: **"Focus ruthlessly on fixing the most serious problems first."**

1. **Make a collective list.** Go around the room; each person names the three most serious problems per session from their notes. Write them on a whiteboard/easel pad. "Me too" = add a checkmark. No discussion yet. Only *observed* problems — things that actually happened in a session.
2. **Choose the ten most serious.** Informal voting; start with the most checkmarks.
3. **Rate them 1–10**, 1 being the worst. Copy to a new list, worst at top, with space under each.
4. **Create the ordered list of fixes.** From the top: a rough idea of how to fix each in the next month, who will do it, resources needed. A fix only needs to move the problem out of the "serious" category — often a tweak, not a complete solution ("the least you can do").
5. **STOP** when the month's available time and resources are allocated. You've got what you came for: a decision and a commitment.

Also keep a **separate low-hanging-fruit list**: things that aren't serious but one person can fix in under an hour without permission from anyone not in the room.

## 12. Deciding what to fix — rules of thumb

- **Serious beats easy.** Don't trade one serious problem for many trivial ones; don't defer with "that's all going to change soon."
- **Resist adding.** When users don't get something, the reflex is to add an explanation or instructions; more often the fix is to remove what obscures the meaning.
- **Distrust feature requests.** Participants aren't designers; a truly great idea announces itself ("Why didn't we think of that?!").
- **Ignore kayak problems** when all three hold: (a) everyone who goes astray notices quickly, (b) they recover without help, (c) it doesn't faze them. "If the user's second guess about where to find things is always right, that's good enough."
- **Grade on a curve** for recruiting mismatches (would our users have had this problem?).
- **Classify** findings to pick fixes: unclear on the concept → fix the big picture (tagline, blurb, page name); the words aren't there → use the user's words, add the missing term; too much going on → cut noise or raise the needed element in the hierarchy.
- Remember it's hard to change a live site later (users resist, side effects) — fix early.

## 13. Alternatives: remote and unmoderated

- **Remote moderated**: participant at home/office via screen sharing; needs broadband and a microphone. Easier to recruit busy people; pool becomes "almost anyone."
- **Unmoderated remote** (e.g., UserTesting.com; Krug discloses compensation from them): send tasks and a link to site/prototype/app; a think-aloud video arrives in about an hour. No live interaction, but cheap and nearly zero effort (no recruiting). Just watch the video.
- Whatever method: "try it, you'll like it" — once you do, you'll keep doing it.

## 14. Checklists

**Before the round**
- [ ] Fixed testing day on the calendar; three participants booked (over-recruit one if possible — extractor note)
- [ ] Incentives ready; permission forms printed
- [ ] What's being tested is available (sketch/wireframe/prototype/live) and reachable from the test machine; demo accounts work
- [ ] 2–5 tasks written, worded completely, with any credentials; participant-choosable details where possible
- [ ] Probing questions collected from the team
- [ ] Test room: quiet, two chairs, computer, mouse, keyboard, mic; browser open to Google
- [ ] Screen sharing running to the observation room; screen recording ready
- [ ] Observation room: big screen, speakers, snacks, three-problems forms
- [ ] Observers invited, including the boss and the boss's boss ("poke your head in")
- [ ] Mobile: camera rig attached to the device; view window open on the laptop; shared and recorded

**During each session**
- [ ] Read the introduction; get the form signed
- [ ] Background questions (2 min)
- [ ] Home page tour: "tell me what you make of it"; no clicking
- [ ] Tasks: think-aloud prompts; no leading; "What would you do if I wasn't here?"
- [ ] Stop a task at done / frustrated / nothing new
- [ ] Probing (5 min) incl. observers' questions
- [ ] Thank, pay, escort
- [ ] Observers write their three most serious problems

**Debrief (lunch)**
- [ ] Collective list of observed problems with checkmarks, no discussion
- [ ] Top ten chosen and ranked 1–10
- [ ] Fix, owner and resources assigned from the top until the month's capacity is used; then stop
- [ ] Low-hanging-fruit list captured
- [ ] Kayak problems and unsupported feature requests set aside
- [ ] Next testing day confirmed
