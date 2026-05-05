# Brainstorming: C-Suite End-to-End Startup Workflow
**Session with Claude Code — May 5, 2026**
*Participants: Anennya*

---

## The Reframe

**Current model:** Sequential founder lifecycle — one person working through stages in order.

**Proposed model:** Parallel C-suite workflows that each run independently but sync at convergence points — like a real company operating.

This is a better mental model because:
1. Real startups don't do these things in sequence — positioning, product, and ops all happen simultaneously
2. It naturally maps to "who owns what" — CMO owns messaging, CPO owns roadmap, CTO owns stack
3. It makes the iterative case obvious — every feature launch, pivot, or new market kicks off the *same sub-workflows* again, not just marketing

---

## Proposed C-Suite Breakdown

| Role | Owns | Maps to Phase 1 |
|---|---|---|
| **CEO** | Vision, strategy, niche, validation, investor narrative | Items 1, 2, 3 |
| **CMO** | Positioning, messaging, promotion, credibility, social | Items 2, 11, 12 |
| **CRO** (Chief Revenue) | Pricing, sales process, first clients, referrals | Items 4, 5, 13 |
| **COO** | Legal/structure, contracts, operations stack, delivery systems | Items 6, 7, 8, 9, 10 |
| **CPO** | Product definition, MVP scope, roadmap, user stories, feature prioritization | (currently missing) |
| **CTO** | Tech stack decisions, engineering workflows, build/ship cycles | (currently missing) |
| **CDO** (Chief Design) | UX, brand, visual identity, design system | (currently missing) |

The CRO was missing from the original design — "find clients" and "pricing" were split between `/pitch` and `/price` but nobody owned the revenue motion end-to-end.

---

## Convergence Points (Where They Sync)

The workflows shouldn't be fully independent — they need to converge at:

1. **Company kickoff** — CEO sets niche + vision; everyone else's workflow inputs from this
2. **Go-to-market** — CMO + CRO sync on message-to-market fit before outreach starts
3. **Feature launch** — CPO defines scope, CTO estimates and builds, CMO announces, CRO prices it
4. **Pivot decision** — CEO triggers a partial reset; CMO re-positions, CPO revises roadmap, CRO updates pricing

---

## The Iterative Trigger Model (Top-Level)

Instead of "run these commands once when you start," the model becomes:

```
Trigger event → which C-suite workflows activate? → converge → ship

New company:      CEO + CMO + CRO + COO (all four at once)
New feature:      CPO + CTO + CMO
Pivot:            CEO + CMO + CPO (+ CRO if pricing changes)
First hire:       COO + CPO (role definition, process handoff)
Fundraise:        CEO + CFO (separate workflow)
New market:       CEO + CMO + CRO
```

---

## CPO Workflow — Product

**What the CPO owns:** What gets built, for whom, and why. The bridge between user needs and what engineering ships.

### Commands

**`/cpo-define`** — *What is this product, exactly?*
- **Inputs:** CEO's niche/ICP, the problem being solved
- **Asks:** Who is the primary user (not the buyer — the user)? What do they do today without this product? What job are they hiring this product to do? What does success look like in their words?
- **Outputs:** Product definition statement (2-3 sentences), 2 user personas with goals and frustrations, the one core use case the MVP must nail
- **Frameworks:** Jobs to Be Done, Product Positioning Canvas
- **Connects to:** Design (personas feed `/design-user`), CEO (validates against niche)

**`/cpo-scope`** — *What's the MVP? What's explicitly NOT in it?*
- **Inputs:** Product definition, rough technical constraints from CTO
- **Asks:** What's the one workflow the product must support end-to-end at launch? What would make a user say "this is worth paying for"? What have we agreed to cut?
- **Outputs:** MVP feature list (Must/Should/Won't — MoSCoW), explicit "out of scope for v1" list, a one-paragraph MVP pitch for the team
- **Frameworks:** MoSCoW, Shape Up "appetite" framing (how much time is this worth?)
- **Connects to:** CTO (`/cto-mvp` uses this directly), Design (`/design-flows` scopes to these features)

**`/cpo-stories`** — *Turn features into buildable requirements*
- **Inputs:** MVP scope
- **Asks:** For each feature: who is doing this action, what are they trying to do, how do we know it worked?
- **Outputs:** User stories in standard format, acceptance criteria per story, AI-specific behavior specs (what the AI should do, how confident it should be, what happens when it fails), edge cases to handle
- **Key addition for AI products:** An "AI behavior card" per feature — expected input, expected output, failure mode, what the user sees when AI is uncertain
- **Connects to:** CTO (stories become tickets in `/cto-sprint`), Design (stories drive `/design-flows`)

**`/cpo-metrics`** — *How do we know if this is working?*
- **Inputs:** Product definition, launch timeline
- **Asks:** What's the one number that tells us this product is working? What does "good" look like at 30/60/90 days?
- **Outputs:** North star metric, 3-5 KPIs with measurement method, success benchmarks at 30/60/90 days, what to watch in week 1 (leading indicators)
- **Frameworks:** AARRR (Acquisition → Activation → Retention → Referral → Revenue), OKRs
- **Connects to:** CEO (revenue metrics), CMO (acquisition metrics), CTO (instrumentation list for `/cto-ship`)

**`/cpo-iterate`** — *User feedback → next thing to build*
- **Inputs:** User feedback, support requests, usage data, team observations
- **Asks:** What are users doing that we didn't expect? What are they asking for repeatedly? What's breaking their flow?
- **Outputs:** Synthesized insight summary, updated priority stack, what to kill/keep/add, one-paragraph brief for next sprint
- **This is the iterative entry point** — every feature cycle starts here after launch

---

## Design Workflow — UX + Brand

**What Design owns:** How the product looks, how it feels to use, and whether users can actually figure it out. Also: the visual identity the company presents to the world.

Two tracks that run in parallel at the start, then converge:

### Brand Track

**`/design-brand`** — *What does this company look and sound like?*
- **Inputs:** CEO's positioning, target user persona, CMO's messaging direction
- **Asks:** Three words that describe the brand personality. Three brands/companies the founder admires visually (and why). What feeling should someone have after their first interaction with the product?
- **Outputs:** Brand brief (color palette direction, typography personality, logo direction, photography/illustration style), voice and tone guide (how we write: formal vs. casual, technical vs. plain, etc.), do/don't examples for brand language
- **Important:** This doesn't replace a designer — it gives a working foundation that can be handed to a designer or used directly in tools like Canva, Figma, or v0
- **Connects to:** CMO (voice and tone feeds all marketing copy), Design UX track (visual direction constrains component choices)

### UX Track

**`/design-user`** — *Who are we designing for and what's their world like?*
- **Inputs:** CPO's user personas (from `/cpo-define`)
- **Asks:** Walk through a day in your user's life. Where does your product fit? What are they doing right before they open it? What are they doing right after? What would make them abandon it?
- **Outputs:** 1-2 rich user personas (goals, frustrations, context of use, tech comfort level, what they already use), user journey map (before/during/after using the product), emotional map (where they feel friction, delight, confusion)
- **Frameworks:** Empathy mapping, Jobs to Be Done for UX
- **Connects to:** CPO (personas validate or challenge `/cpo-define`), `/design-flows`

**`/design-flows`** — *How does the user actually move through the product?*
- **Inputs:** CPO's user stories, user personas, MVP feature list
- **Asks:** Walk through the user's first 5 minutes. What's the first thing they see? What's the first action they take? Where do they get confused?
- **Outputs:** Core user flow descriptions (text-based, since Claude produces text not wireframes), screen list with purpose of each screen, key decision points (where the user makes a choice), navigation structure, prompts formatted for Figma/v0/Midjourney to generate actual wireframes
- **AI-specific flows:** How the AI interaction is surfaced (input → loading state → output → feedback mechanism), what the user sees when AI is uncertain or wrong, how to handle AI latency

**`/design-system`** — *Reusable patterns so design scales*
- **Inputs:** Brand brief, core user flows
- **Asks:** What components appear on more than 2 screens? What interactions repeat?
- **Outputs:** Design token list (colors, spacing, type scale — formatted for Tailwind, CSS variables, or Figma tokens), component checklist (which components to build first), AI-specific component patterns (loading skeletons for AI responses, confidence indicators, "AI generated" labels, regenerate buttons)
- **When to use:** After the first 3 flows are defined — not before

**`/design-test`** — *Does this actually work for real users?*
- **Inputs:** Live product or prototype URL, specific flows to test
- **Asks:** What's the one thing we most need to learn from users right now?
- **Outputs:** 5-task usability test script, 3-question post-task interview guide, what to watch for (common failure patterns), how to synthesize results back into `/cpo-iterate`
- **Frameworks:** Nielsen's 5-user rule (5 users find 85% of usability problems), think-aloud protocol

---

## CTO/Engineering Workflow

**What the CTO owns:** What the product is built with, how it's built, and whether it stays up. For non-technical founders, this workflow is about making good technology decisions, not writing code.

**Two modes designed in from the start:**
- **Decision mode** — for non-technical founders who need to understand and approve technology choices
- **Build mode** — for technical founders/CTOs who are actually implementing

### Commands

**`/cto-stack`** — *What do we build this with?*
- **Inputs:** Product type (web app, mobile, automation, API, etc.), team's existing skills, budget, launch timeline
- **Asks:** Who will maintain this after launch — same team or someone new? How much do we expect this to scale in year 1? Is this a prototype or the real thing?
- **Outputs:** Recommended stack with plain-English rationale per choice, cost estimate (infra + tooling per month), trade-offs of each major choice, what's easy to change later vs. what's hard to undo, red flags to avoid
- **AI-specific decisions:** Which LLM for which task (reasoning vs. speed vs. cost), API vs. self-hosted, RAG architecture decision, when fine-tuning is worth it (almost never at MVP stage)
- **Connects to:** CPO (technical constraints feed `/cpo-scope`), Design (framework choice affects component library)

**`/cto-architecture`** — *How does the system fit together?*
- **Inputs:** Stack selection, MVP scope from CPO
- **Asks:** What data does this product store and who owns it? What are the three most important things that must not break?
- **Outputs:** Plain-English architecture description (component diagram in text/Mermaid), key architecture decisions documented (ADR format — what we decided, why, what we considered), data model basics, API surface (what endpoints exist and what they do), AI integration points (where LLM calls happen, how they're managed)
- **ADR format matters here** — decisions documented so the team can revisit them, not just the current choice
- **Connects to:** Design (API surface informs what's possible in flows), CPO (surfaces constraints that affect scope)

**`/cto-mvp`** — *Engineering scope and build order for MVP*
- **Inputs:** CPO's user stories, CPO's MVP scope
- **Asks:** What has to work for any other thing to work? What can we fake with a human in the loop before we automate it?
- **Outputs:** Engineering estimate (rough, in weeks not hours), build order with dependency chain, a "fake it" option for each feature (what can be done manually before it's automated), what to cut if behind schedule, what stays in v2
- **Key principle:** The "Wizard of Oz" test — what can a human do behind the scenes that looks like the product working? This extends the MVP principle into engineering.
- **Connects to:** CPO (estimate feeds roadmap confidence), Design (build order tells Design what to finish first)

**`/cto-sprint`** — *What are we building this week?*
- **Inputs:** Current CPO priorities, what design has finalized, team capacity
- **Asks:** What did we commit to last week and is it done? What's blocking anyone?
- **Outputs:** Sprint goal (one sentence), broken-down task list with estimates, explicit dependencies (what needs Design to finish first, what needs CPO sign-off), blockers surfaced, which tasks need pairing or review
- **For solo founders:** Weekly priority list instead of sprint — same structure, no ceremony
- **Connects to:** CPO (sprint output = what ships, which feeds `/cpo-metrics`), Design (flags what Design artifacts are needed and when)

**`/cto-ship`** — *Deployment and release process*
- **Inputs:** What's being shipped, current environment setup
- **Asks:** What's the rollback plan if this breaks? Who do we tell when this goes live?
- **Outputs:** Pre-launch checklist (env vars set, migrations run, error monitoring live, AI API limits set), deployment steps, post-launch health checks (what to watch in the first 30 min), rollback procedure, launch signal for CMO/CPO
- **AI-specific checklist:** Rate limits configured, cost alerts set, fallback behavior defined (what happens when the LLM call fails), latency baseline measured
- **Connects to:** CMO (launch signal triggers announcement), CPO (triggers metric tracking)

**`/cto-ai`** — *AI integration decisions* *(unique to AI startups — no equivalent in a traditional startup toolkit)*
- **Inputs:** Features that use AI (from CPO's stories), stack selection
- **Asks:** What does the AI need to do reliably? What's acceptable failure rate? How do we know it's working well?
- **Outputs:** Model selection per task with cost/latency trade-offs, prompt management strategy (where prompts live, how they're versioned, how they're tested), evaluation framework (how to measure AI output quality — human eval, automated, or both), cost monitoring setup, RAG decision (do we need it? what goes in the vector store?)
- **This command is the bridge between product and engineering for AI features** — connects CPO's AI behavior cards to actual implementation decisions

**`/cto-review`** — *What's slowing us down and what do we fix next?*
- **Inputs:** Recurring problems, slow areas, team pain points
- **Asks:** What takes longer than it should? What are we afraid to touch? What's been patched more than twice?
- **Outputs:** Technical debt register (what it is, why it matters, effort to fix), prioritized improvement list, recommendation on what to refactor vs. what to rebuild, when to schedule cleanup sprints

---

## How the Three Workflows Connect

```
CEO sets niche/ICP
       ↓
CPO: /cpo-define ──────────────────→ Design: /design-user (personas)
       ↓                                        ↓
CPO: /cpo-scope ────────────────────→ Design: /design-flows
       ↓              ↘                         ↓
CTO: /cto-stack        CTO: /cto-mvp ← CPO stories + design flows
       ↓                    ↓
CTO: /cto-architecture      ↓
                       CTO: /cto-sprint (weekly)
                            ↓
                       CTO: /cto-ship
                            ↓
                    CMO announces ←────────────────
                    CPO measures metrics
                    CPO: /cpo-iterate ──────────→ loop back
```

**Three hard handoff points where work must pass between roles:**

| Handoff | From → To | Artifact passed |
|---|---|---|
| Feature definition | CPO → Design + CTO | User stories + AI behavior cards |
| Design ready | Design → CTO | Finalized flows + component specs |
| Ship ready | CTO → CMO + CPO | Launch signal + what to measure |

---

## The Iterative Trigger Model (CPO + Design + CTO)

| Trigger | CPO | Design | CTO |
|---|---|---|---|
| **New startup** | define → scope → stories → metrics | brand → user → flows → system | stack → architecture → mvp → sprint → ship |
| **New feature** | scope (scoped) → stories | flows (new screens only) | mvp (feature) → sprint → ship |
| **User feedback** | iterate → update scope | design-test → update flows | review (if tech cause) → sprint |
| **Pivot** | define (reset) → scope (new) → stories | user (new) → flows (new) | architecture (what carries?) → mvp (new) |
| **First hire** | cpo-stories (role handoff) | design-system (hand off to new designer) | cto-architecture (onboarding doc) |

---

## What's Unique to AI Startups Across All Three

Most startup workflow toolkits don't account for these — they need to be woven into every relevant command:

- **CPO:** AI behavior cards (expected output, failure mode, user-facing error state) per feature
- **Design:** AI interaction patterns (loading states, confidence indicators, "regenerate" affordances, trust signals)
- **CTO:** Model selection, prompt versioning, evaluation framework, cost monitoring, rate limit handling

This is the differentiated layer vs. a generic startup toolkit — and it's directly relevant to everything the WDAI community is building.

---

## Open Questions / Next Steps

- [ ] Design the shared **product brief** document that all three roles read from and write back to — the connective tissue between parallel workflows
- [ ] Draft actual command files (`.md` format for `.claude/commands/`) for priority commands
- [ ] Pick a test case startup idea (from the WDAI community or a hypothetical) to walk through all three workflows end-to-end
- [ ] Define the CEO, CMO, CRO, and COO workflows at the same level of detail
- [ ] Decide: does each C-suite workflow live in its own folder, or as commands with a role prefix?
