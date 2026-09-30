# Yway — Greenfield Product & AI-Agent Development Idea

## 1. Purpose of This Document

This file captures the founder's current product intent for a **new greenfield Yway repository**.

It is written to be used by the founder together with Codex and Matt Pocock's engineering skills while designing and building the product from scratch.

Until the project deliberately creates more specific product specifications and decision records, this file is the primary statement of founder intent.

Agents must not silently reinterpret unresolved product or business decisions.

For decisions that require founder judgment:

- research facts independently,
- explain realistic options and trade-offs,
- make a recommendation when useful,
- then wait for the founder's decision.

---

# Product

## 2. Product Vision

Yway is an interactive career simulation-to-work platform for young people in Myanmar.

Yway does not primarily teach young people _about_ careers.

Instead, Yway lets a young person temporarily step into a career and experience what doing that work feels like through short, interactive, career-specific simulations inside the app.

> **Career အကြောင်းသင်ပေးတာမဟုတ်ဘူး။ ခဏလောက် အဲ့ဒီ career ထဲမှာ အလုပ်ဝင်လုပ်ကြည့်ခိုင်းတာ။**

English equivalent:

> **Do not explain the career first. Let the user do a realistic slice of the work.**

The user should feel:

> **“I am not reading about this career. I am temporarily doing this job.”**

---

## 3. Core Journey

The intended Yway journey is:

**Discover Career  
→ Enter Career Simulation  
→ Do Realistic Work  
→ Experience Decisions / Trade-offs / Pressure  
→ Receive Contextual Feedback  
→ Reflect  
→ Choose a Reversible Direction  
→ Learn with Career Experts  
→ Practice  
→ Build Evidence  
→ Complete Employer Quests  
→ Browse Relevant Jobs  
→ Apply Voluntarily  
→ Employer Review  
→ Interview  
→ Offer  
→ Hire**

The journey starts with experience before commitment.

The intended order is:

> **Try → Understand → Decide Whether to Learn**

not:

> **Learn → Try**

---

## 4. Career Simulation Experience

### 4.1 Career Experience Packs are simulations

A Career Experience Pack is not mainly an article, course, questionnaire, or quiz.

It is an interactive, career-specific simulation that recreates a realistic slice of work.

Each career should have its own simulation experience.

Examples:

- Customer Support → inbox / ticketing-style interface
- Accounting → spreadsheet / invoice / reconciliation-style interface
- Software Development → ticket / editor / debugging-style interface
- Digital Marketing → campaign brief / audience / budget / result dashboard
- UI/UX Design → design brief / user-flow / critique-style interface
- Retail → customer interaction / inventory / prioritization flow

The product must not reduce all careers to the same multiple-choice template.

### 4.2 Mission-based structure

Each career contains multiple short missions.

Typical mission duration:

**5–10 minutes**

A career may contain:

**Mission 1  
→ Mission 2  
→ Mission 3  
→ Mission 4  
→ deeper / harder missions**

### 4.3 Mission trees

Mission progression should support branching.

The next situation may change depending on the user's meaningful work decision.

Example:

**Customer complaint  
→ User writes response  
→ System interprets response  
→ Consequence occurs  
→ Recovery / escalation / resolution branch  
→ Continue**

Branches should represent realistic work consequences rather than arbitrary game choices.

### 4.4 Career-specific UI

The app should mimic the relevant type of work environment where useful.

Possible simulation surfaces include:

- simulated inbox
- spreadsheet-like screen
- ticket system
- campaign dashboard
- document review
- design brief
- workflow queue
- customer conversation
- error review screen
- task board
- code/debugging-like environment

The simulation does not need to copy real commercial software exactly.

It should reproduce the important _work interaction_ clearly enough that the user feels they are doing the job.

### 4.5 Users do real work

Users should not only select predefined answers.

Where appropriate, they should:

- write responses
- create small artifacts
- explain decisions
- review documents
- prioritize work
- spot errors
- handle simulated conversations
- choose workflows
- inspect information
- respond to unexpected events

The experience should feel active rather than instructional.

---

## 5. Duolingo-like Interaction Philosophy

Yway should feel closer to a Duolingo-style interactive experience than to reading a course.

This means interaction quality, not copying Duolingo's visual design or reward system.

Desired qualities:

- bite-sized missions
- one clear task at a time
- low-friction interaction
- immediate contextual feedback
- visible progress through work
- satisfying completion moments
- gradually increasing realism and difficulty
- app-native interaction
- replay and practice where useful

Progress should represent real work, for example:

- Mission 2 of 5
- Client brief handled
- Customer reply sent
- Reconciliation step completed
- Debugging step completed

Do not make the core experience depend on:

- career-fit percentages
- employability scores
- candidate-quality scores
- deterministic career rankings
- competitive leaderboards
- points as the main progress model
- streak pressure as the main progress model

---

## 6. Consequences Instead of Game Over

Poor decisions should not normally produce a “Game Over” screen.

Preferred pattern:

**User Action  
→ Realistic Consequence  
→ Contextual Feedback  
→ Recovery / Changed Situation  
→ Continue**

A poor customer response might create an escalation.

The user then experiences what handling the escalation feels like.

Mistakes are part of learning what the work is actually like.

---

## 7. AI in the Simulation

### 7.1 Initial simulation creation

At the beginning, Yway will use AI heavily to create simulations.

AI may assist with:

- career research
- scenario generation
- mission design
- work artifacts
- branching paths
- consequences
- feedback drafts
- simulation UI concepts
- localization drafts
- review support

A Lead Career Expert is not required for the first version of a simulation.

### 7.2 Simulation provenance

Simulation provenance must be transparent.

Possible lifecycle:

**AI Generated  
→ Founder / Yway Reviewed  
→ Expert Reviewed**

If a career expert has not reviewed a simulation, the product should clearly say so.

When a qualified Lead Career Expert later reviews the exact simulation version, its status can be changed to reflect that review.

AI generation must never be presented as expert verification.

### 7.3 AI feedback

AI may provide contextual qualitative feedback on open-ended work.

AI should act more like a contextual coach than a judge.

Feedback may cover:

- what happened because of the user's action
- what the user handled well
- what context may have been missed
- realistic trade-offs
- what to notice next
- what happens next
- a reflection prompt

AI should not output:

- career-fit score
- employability score
- capability score
- candidate score
- deterministic career verdict

### 7.4 Preferred initial runtime model

Do not make the simulation fully open-ended and controlled entirely by AI at runtime.

Preferred starting architecture:

\*\*Authored Mission Tree

- Deterministic State / Branch Logic
- AI for bounded interpretation and qualitative feedback\*\*

Example:

**User writes a response  
→ AI evaluates it against mission context / rubric  
→ System maps it to one of the allowed branches  
→ Branch consequence appears**

This is preferred because it is easier to test, debug, control, price, and operate as a solo developer.

---

## 8. Simulation Core Domain

Initial domain concepts:

1. Career
2. Simulation
3. Mission
4. Mission State
5. User Action
6. Branch
7. Consequence
8. AI Feedback
9. Reflection
10. Simulation Review Status

Reusable simulation primitives may include:

- read
- inspect
- choose
- write
- sort
- prioritize
- respond
- create
- compare
- spot errors
- handle conversation
- review a document
- see consequences
- receive feedback
- reflect

The desired architecture principle is:

> **Reusable interaction primitives → Career-specific composition → Unique realistic work experience**

A reusable simulation engine is valuable only if it preserves the unique feel of each career.

---

## 9. Career Expert Model

Yway is not an open creator marketplace.

A career may have one active Yway-selected **Lead Career Expert**.

Other people may also participate, such as:

- guest experts
- reviewers
- workshop speakers
- facilitators
- specialist contributors

The Lead Career Expert may contribute to:

- career reality
- simulation realism review
- learning experiences
- workshops
- guided practice
- Q&A
- scoped work review

A Lead Career Expert is **not required** before the first simulation is released.

AI-generated simulation status must remain visible until stronger review exists.

---

## 10. Learning After Simulation

Simulation is career discovery.

Paid learning is an optional deeper layer.

If a user wants to continue, the selected expert may provide:

- courses
- workshops
- guided practice
- live sessions
- Q&A
- practical assignments
- work review
- supporting resources

The product should preserve the user's ability to:

- go deeper
- try another career
- compare experiences
- pause

---

## 11. Paid Learning Business Model

Experts can earn from approved paid learning experiences.

Price should be agreed by:

**Yway + Career Expert**

Possible transaction flow:

**Youth purchases learning experience  
→ Payment processed  
→ Expert earning recorded  
→ Yway commission recorded**

Exact commercial terms are not decided yet.

Payment must not buy:

- favorable evaluation
- better career direction
- ranking
- hiring priority
- stronger evidence classification

---

## 12. Evidence Portfolio

The user should own a private Evidence Portfolio.

Evidence types must remain distinct.

Examples:

- Exploration signals
- Practice evidence
- Verified assessment evidence
- User-added work
- Employer Quest work

Simulation completion does **not** automatically prove professional capability.

Simulation activity must not silently become verified evidence.

Users control what they:

- organize
- hide
- export
- share

Employers should only receive explicitly authorized information.

---

## 13. Employer Quests

An Employer Quest is a real-world business challenge supplied by a company and structured / reviewed by Yway.

Preferred flow:

**Company creates Quest draft  
→ Yway reviews / structures it  
→ Quest is approved  
→ Quest is published  
→ Youth participates voluntarily  
→ Youth explicitly submits work**

A Quest is not:

- a normal career simulation
- a course
- a job application
- an automatic hiring competition

Quest completion does not automatically create candidate status.

---

## 14. Jobs and Hiring

Yway should support relevant real job opportunities without becoming an undifferentiated job-board aggregator.

Recruitment begins only when a user explicitly applies to a Yway job.

Hiring lifecycle:

**Yway Job  
→ User Applies  
→ Employer Review  
→ Interview  
→ Offer  
→ Hire**

Browsing, simulation activity, learning, practice, and Quest completion do not automatically create candidate status.

---

## 15. Hiring Success Fee

Yway earns a hiring success fee only when the hire is attributable to a Yway job application.

Intended attribution:

**Job published on Yway  
→ User applies through Yway  
→ Employer hires that user  
→ Hire is confirmed  
→ Employer owes Yway a success fee**

If the same person is hired outside the Yway job/application flow, that should not automatically create a Yway success fee.

Exact success-fee pricing is not decided yet.

Youth must never pay recruitment or placement fees.

---

## 16. Main Actors

### Youth

**Discover  
→ Simulate  
→ Reflect  
→ Learn  
→ Practice  
→ Build Evidence  
→ Quest  
→ Jobs  
→ Apply  
→ Interview  
→ Offer  
→ Hire**

### Lead Career Expert

Possible responsibilities:

- career-reality contribution
- simulation review
- learning experiences
- guided practice
- workshops
- Q&A
- scoped work review

Experts may earn money from paid learning.

### Employer

Possible capabilities:

- company onboarding
- Employer Quest drafts
- job publishing
- application review
- interview tracking
- offer tracking
- hire confirmation
- Yway billing

### Yway Team / Admin

Possible operations:

- career management
- simulation review
- expert selection
- company verification
- Quest approval
- content moderation
- learning commerce
- expert earnings / payouts
- employer billing
- hiring success-fee tracking
- support
- privacy / consent operations

---

## 17. Production V1 Launch Philosophy

Yway should not publicly launch as a thin feature-only MVP if the intended V1 journey is incomplete.

Closed and internal validation before public launch is expected.

Preferred sequence:

**Build intended Production V1  
→ Internal QA  
→ Closed end-to-end validation  
→ Fix critical issues  
→ Production-readiness validation  
→ Release Candidate  
→ Public Production V1**

The public-launch gate is not primarily the number of careers.

> **Every career selected for public launch should support the intended full end-to-end journey.**

The exact number of launch careers is not decided yet.

---

## 18. Non-Negotiable Product Principles

- Try before choosing.
- Career guidance remains reversible.
- Simulation produces clues, not destiny.
- No universal “best career”.
- No career-fit percentage.
- No employability score.
- No hidden candidate score.
- No deterministic career ranking.
- Exploration ≠ Practice ≠ Verified Assessment.
- Employer Quest ≠ Employment Application.
- Quest completion does not automatically create candidate status.
- Employers do not automatically receive private exploration data.
- Sharing is explicit and purpose-specific.
- Youth never pay recruitment or placement fees.
- Payment cannot buy evaluation, ranking, direction, or hiring priority.
- AI-generated simulation must disclose its status.
- AI generation is not expert review.
- User value exists before employer value.
- Public launch happens only after the intended V1 is production-ready.

---

## 19. Important Decisions Already Made

### Product

- Yway is a career simulation-to-work platform.
- Career discovery starts with realistic work experience.
- Public launch waits for the intended V1 journey to be complete for selected launch careers.

### Simulation

- Careers contain multiple missions.
- Each mission is approximately 5–10 minutes.
- Mission paths can branch.
- Career-specific UI should mimic the relevant work environment where useful.
- Users should perform open-ended work, not only choose predefined answers.
- User decisions can change the scenario.
- Poor decisions produce realistic consequences and continuation rather than normal Game Over.
- AI may provide qualitative contextual feedback.
- Initial simulations may be AI-generated.
- Lead Career Expert is not required before a simulation exists.
- AI-generated status must be visible.
- Expert-reviewed status is added only after appropriate expert review.

### Expert

- Yway is not an open creator marketplace.
- One active Lead Career Expert per career is the intended model.
- Guest experts / reviewers / speakers / facilitators may also exist.
- Paid learning price is agreed by Yway and the expert.

### Hiring

- Success-fee attribution applies to hires coming from a Yway job application.
- Youth do not pay recruitment or placement fees.

### Tooling / Development

- This is a new greenfield repository.
- Development will be AI-agent-assisted.
- Codex will be a primary implementation agent.
- Matt Pocock's engineering skills will be used as the development workflow.
- pnpm is the package manager.
- The founder's strongest implementation experience is React, Next.js, React Native, TypeScript, and frontend development.
- Architecture should remain manageable for a solo developer.
- Avoid premature microservices.

---

## 20. Decisions Still Open

Agents must not silently invent answers to these.

### Simulation

- exact mission-tree authoring format
- number of missions per career
- branch convergence / termination model
- replay rules
- difficulty progression
- AI feedback rubric design
- how open-ended input maps to bounded branches
- simulation versioning
- exact owner-review gate for AI-generated simulations
- what simulation activity is persisted offline

### Experts / Learning

- exact expert qualification requirements
- expert replacement lifecycle
- ownership of expert-created learning material
- refund policy
- learning commission amount
- payout timing and mechanism

### Hiring / Commerce

- hiring success-fee amount
- exact hire-confirmation rules
- hiring attribution dispute handling
- employer billing terms
- payment provider

### Technical

- monorepo vs other repository layout
- exact frontend application boundaries
- exact backend architecture
- authentication provider
- database
- file / object storage
- AI provider / model strategy
- AI provider abstraction
- hosting / deployment
- notification system
- analytics / observability
- offline / sync architecture
- content authoring system
- final Partner Portal vs separate Expert / Employer portals

### Launch

- initial launch career count
- exact end-to-end launch readiness checklist
- exact policy when a selected career has no current Quest or live job

Use structured decision-making before implementation.

---

# Greenfield AI-Agent Development

## 21. Founder and Agent Responsibilities

### Founder owns

The founder owns decisions about:

- product meaning
- user experience
- business model
- trust boundaries
- monetization intent
- launch scope
- final trade-offs

### AI agents own the legwork

Agents should:

- inspect the repository
- research technical facts
- compare implementation options
- prototype alternatives
- write specifications
- create tickets
- implement approved work
- write tests
- run verification
- review diffs
- document decisions

Agents should not silently turn technical convenience into a product decision.

When the founder lacks technical knowledge, the agent should explain options and recommend a sensible default rather than asking the founder to research it manually.

---

## 22. Initial Source-of-Truth Model

This is a new repository, so keep the authority model simple.

Initially:

1. `idea.md` — founder product intent
2. `GLOSSARY.md` — canonical domain terminology
3. `docs/adr/` — accepted hard-to-reverse technical / architectural decisions
4. GitHub Issues — Wayfinder maps, decision tickets, specs, and implementation tickets
5. Code and tests — implemented behavior

`idea.md` should not become an implementation dump.

As the project matures, product specifications may be split into more focused documents, but do not create document bureaucracy before it is useful.

If another document contradicts `idea.md` on unresolved founder intent, surface the conflict instead of silently choosing one.

---

## 23. Matt Pocock Skills Workflow

Install the skills with pnpm:

```bash
pnpm dlx skills@latest add mattpocock/skills
```

Recommended skills for Yway:

- `setup-matt-pocock-skills`
- `wayfinder`
- `grill-with-docs`
- `domain-modeling`
- `prototype`
- `research`
- `to-spec`
- `to-tickets`
- `implement`
- `tdd`
- `code-review`
- `pr`
- `retro`
- `writing-for-agents`

The main development flow should be:

**idea.md  
→ setup-matt-pocock-skills  
→ Wayfinder  
→ grill-with-docs + domain-modeling  
→ prototype where a concrete experience is needed  
→ resolved decisions  
→ to-spec  
→ to-tickets  
→ implement + TDD  
→ code-review  
→ PR + CI  
→ human merge  
→ retro**

For large work, do not jump directly from idea to implementation.

---

## 24. Repository Bootstrap

Start with a minimal repository.

Suggested initial state:

```text
/
├── idea.md
└── README.md
```

Then run:

```bash
pnpm dlx skills@latest add mattpocock/skills
```

After installation, ask Codex to run `setup-matt-pocock-skills`.

Use:

- GitHub Issues as the issue tracker
- the default triage labels unless there is a clear reason to change them
- single-context domain docs initially unless the repository later genuinely becomes a large multi-context monorepo

Do not decide the application architecture merely because a tool or template suggests one.

---

## 25. First Codex Task — Configure the Repository

Give Codex:

```text
Read idea.md completely.

This is a new greenfield Yway repository.

Run /setup-matt-pocock-skills.

Use GitHub Issues as the issue tracker.

Use pnpm for package management.

Treat idea.md as the founder's current product intent.

This project will be built primarily with AI agents, especially Codex.

Keep the initial agent/document system small and easy to navigate.

Before making changes:
1. inspect the repository,
2. explain what setup-matt-pocock-skills wants to add or change,
3. identify any decision that actually needs my input.

Do not start implementing Yway product features.

After setup, show:
- files created or changed
- issue-tracker configuration
- domain-doc configuration
- triage labels
- how future agents should find idea.md
```

---

## 26. Second Codex Task — Wayfind the Product

After repository setup, give Codex:

```text
Read idea.md completely.

Use /wayfinder.

This is a greenfield product being built from scratch with AI agents.

Destination:

Create a build-ready product and technical path for Yway, an interactive career-simulation-to-work platform where young people temporarily do realistic work through short branching missions, receive contextual AI feedback, reflect, and can later move into learning, practice, evidence, Employer Quests, jobs, applications, interviews, offers, and hires.

The founder decisions in idea.md are intentional unless explicitly revisited.

Do not implement the product yet.

Facts are your responsibility to investigate.
Product and business decisions are mine.

Do not answer HITL questions for me.

When a technical decision is outside my expertise:
- research realistic options,
- explain trade-offs in plain language,
- recommend a sensible default for a solo TypeScript / React / React Native developer,
- then let me decide.

Pay special attention to:
- Career Simulation Experience Model
- Mission / Simulation domain language
- mission tree and branch semantics
- career-specific simulated work UI
- open-ended user actions
- AI feedback and bounded branch classification
- simulation authoring and content format
- provenance and review status
- persistence and offline behavior
- identity and authentication
- Evidence Portfolio
- expert system
- learning commerce
- Employer Quests
- jobs and application lifecycle
- interview / offer / hire
- hiring attribution
- employer billing
- admin operations
- application boundaries
- backend architecture
- database
- AI provider strategy
- payments
- release readiness

Create:
- one Wayfinder map
- only the first decision frontier that is clear enough to specify
- fog-of-war notes for later decisions

Stop after charting the map and first frontier.
Do not implement product features.
```

---

## 27. Work Through Wayfinder Decisions

Resolve one decision ticket at a time.

Use:

- `grill-with-docs` for founder decisions
- `domain-modeling` to keep terminology precise
- `research` when external technical facts are needed
- `prototype` when the answer depends on seeing or using something

Do not build production code merely to avoid making a decision.

Do not pre-decide every future detail.

Use Wayfinder's fog-of-war approach: make only the decisions that are currently sharp enough to make.

---

## 28. Prototype the Core Experience Before Production Architecture

The hardest product question is not authentication or database choice.

It is whether a Career Simulation actually feels like temporarily doing the job.

Before building a large generic engine, prototype one representative career.

A good initial tracer career could be Customer Support because it naturally supports:

- simulated inbox
- open-ended writing
- branching consequences
- escalation
- recovery
- contextual feedback

Prototype goal:

> **Does this feel like doing the job rather than learning about the job?**

Example Codex prompt:

```text
Use /prototype.

Create a throwaway mobile-first prototype for one Yway Customer Support mission.

The prototype exists to answer one question:

“Does this feel like temporarily doing the job rather than learning about the job?”

Experience requirements:
- simulated support inbox
- realistic customer message
- user writes their own reply
- AI feedback may be mocked
- the reply maps to one of several bounded branches
- a realistic consequence appears
- a poor decision does not cause Game Over
- the user continues into a recovery / changed situation
- reflection appears at the end
- total mission should feel like a 5–10 minute work slice
- game-like interaction quality
- no points, streaks, career score, or leaderboard

Do not create production infrastructure.
Do not choose the final backend architecture from this prototype.
```

Prototype lessons should feed back into Wayfinder decisions and later specs.

---

## 29. First Production Spec

Once the first simulation decisions are clear and the prototype has taught enough, use `to-spec`.

The first production specification should focus on **one real end-to-end career simulation vertical**, not “build the entire Yway platform” and not “build a universal simulation engine for every future career”.

The first spec should define enough to implement:

- Career
- Simulation
- Mission
- Mission State
- User Action
- Branch
- Consequence
- AI Feedback
- Reflection
- Simulation Review Status
- persistence needed for this vertical
- reusable interaction primitives actually needed
- career-specific simulated UI needed
- AI boundary
- test seams
- provenance display

Example prompt:

```text
Use /to-spec.

Create the first production implementation spec for Yway's Career Simulation vertical.

Use:
- idea.md
- GLOSSARY.md
- accepted ADRs
- resolved Wayfinder decisions
- lessons from the approved prototype

Goal:

Implement one representative career simulation end-to-end so that a user can enter a career, complete a realistic 5–10 minute mission, perform open-ended work, receive bounded qualitative AI feedback, experience a branch consequence, continue after a poor decision, complete reflection, and preserve progress.

Do not optimize for every hypothetical future career.

Prefer simple architecture suitable for a solo TypeScript / React / React Native developer working with AI agents.
```

---

## 30. Convert Specs into Vertical Tickets

Use `to-tickets`.

Do not create horizontal tickets such as:

- create database
- build backend
- build UI
- add tests

Prefer tracer-bullet tickets such as:

- user can open a career and begin Mission 1 end-to-end
- user can submit an open-ended work response
- bounded AI interpretation maps a response to an allowed branch
- branch consequence appears
- user continues after a poor decision
- reflection is saved
- AI-generated provenance is visible

Each ticket should be independently demoable or verifiable.

---

## 31. Implementation Loop

For each ready ticket:

1. Start with a fresh agent context when practical.
2. Read the ticket and referenced source material.
3. Read relevant `idea.md`, glossary terms, and ADRs.
4. Use `tdd` at agreed seams.
5. Implement only the ticket's vertical slice.
6. Run targeted typechecks / tests regularly.
7. Run the full required verification before declaring the ticket complete.
8. Run `code-review`.
9. Fix material findings.
10. Create or update the PR using `pr`.
11. Let CI run.
12. Human reviews and merges.
13. Use `retro` after meaningful work, especially when the agent workflow failed or created repeated friction.

Never claim a check passed unless it actually ran.

---

## 32. AI-Agent Engineering Rules

### Keep tasks small

Do not tell an agent:

> “Build Yway.”

Prefer:

> “Implement the next approved vertical ticket.”

### Keep product decisions explicit

AI can recommend.

AI should not silently decide:

- business rules
- trust policy
- monetization
- user privacy behavior
- launch scope

### Prefer tests over trust

Agent-generated code should be validated by:

- type checking
- unit / integration tests where appropriate
- behavior tests at stable seams
- code review
- CI

### Prefer simple architecture

The founder is a solo developer.

Avoid architecture that needs a large operations team unless there is a demonstrated need.

### Avoid premature abstraction

Do not build a universal career simulation engine before one real simulation proves which abstractions are actually needed.

Use the first tracer career to discover the architecture.

### Keep agent navigation clear

Use `writing-for-agents` principles:

- one source of truth per meaning
- concise AGENTS.md
- context pointers instead of duplicated rules
- glossary for domain language
- ADRs only for meaningful hard-to-reverse trade-offs

---

## 33. Technical Biases, Not Final Decisions

The founder's current skills make these practical defaults worth considering:

- TypeScript
- React Native for the Youth mobile app
- React / Next.js for web surfaces
- pnpm
- a small number of deployable applications
- shared types / domain code where it genuinely helps
- one primary backend before considering multiple services
- bounded AI calls through server-side code
- no AI API secrets in the mobile client
- deterministic mission state where possible
- no premature microservices

These are **biases**, not final architectural decisions.

Use Wayfinder / research / ADRs before locking significant architecture.

---

## 34. Suggested Product Build Direction

This is a directional sequence, not a rigid roadmap.

**Career Simulation foundation  
→ Mission persistence / branching  
→ AI feedback  
→ Reflection / reversible direction  
→ Simulation authoring workflow  
→ Practice and Evidence  
→ Identity / Consent / Sharing  
→ Expert system  
→ Paid learning / Commerce  
→ Employer Quest  
→ Jobs / Applications  
→ Interview / Offer / Hire  
→ Hiring attribution / Employer Billing  
→ Admin / Operations  
→ Cross-surface integration  
→ Localization / Accessibility  
→ Security / Reliability / Observability  
→ Closed end-to-end validation  
→ Release Candidate  
→ Production V1**

Public launch should happen after the intended selected-career journey is production-ready.

Internal and closed testing should happen throughout development.

---

## 35. Definition of Success

Yway succeeds when a young person can say:

> **“ဒီ career ကဘယ်လိုလဲဆိုတာ ငါဖတ်ပြီးသိတာမဟုတ်ဘူး။ ငါကိုယ်တိုင် ခဏဝင်လုပ်ကြည့်ပြီး နားလည်သွားတာ।”**

And when the complete platform can move that person from realistic career experience to a voluntary, trusted path toward learning, evidence, company work, and eventually a real job—without taking control of their future away from them.
