# CPO Frameworks — Evergreen Best Practices

**Session with Claude Code — May 12, 2026**
*Participant: Aparna*
*Purpose: Identify the evergreen, best-practice frameworks the CPO (Chief Product Officer) role should draw from, sourced from leading product thought leadership and books that have stood the test of time. Reconciles with Anennya's May 5 CPO command design. Command naming follows a beginner-friendly logic.*

> **Scope note (important):** CPO is built for the **apps and workflows tracks only** in this iteration. Pure consultants do not need it yet — their "product" is their expertise and service, not software. A consulting-lite path can be added in a later iteration.

---

## How a CPO Operates — Explained to a Beginner Founder

**The one-line version:** If the CEO decides *what business you're in*, the CPO decides *what you actually build* — for whom, and why. They're the bridge between "people have this problem" and "here's the thing that solves it."

Think of it this way:
- The **CEO** says: "We help solo HR consultants save time on client reporting."
- The **CPO** says: "So the product is a tool that pulls from their existing systems and drafts a report in under 10 minutes. Here's exactly what it does in v1, here's what it deliberately does NOT do, and here's how we'll know if it's working."

### The four things every CPO really does

1. **Defines the product.** Who's the actual *user* (not just the buyer)? What job are they hiring this product to do? What's the one thing it must nail?
2. **Decides what's in and what's out.** The hardest and most valuable job — ruthlessly scoping the MVP. What's the smallest thing that's still worth paying for? What are we *not* building in v1? Most product failures come from building too much.
3. **Turns ideas into buildable requirements.** Translates "it should help them write reports" into specific, testable requirements a developer (or Claude Code) can actually build.
4. **Measures whether it's working.** Defines the one number that tells you the product is succeeding, and what "good" looks like at 30/60/90 days.

### The mindset shift that defines the role

The biggest reframe — from Marty Cagan, the most influential product thinker alive:

> **Build to solve a problem, not to ship a feature.**

Beginners think product work is a to-do list of features ("add login, add dashboard, add export"). Real product work is the opposite: you're handed a *problem* and your job is to discover the smallest solution that actually works. Cagan's test for a good product: **valuable, usable, feasible, and viable** — desirable to users, easy to use, possible to build, and good for the business.

The second reframe, unique to AI products: **decide what happens when the AI is wrong.** A traditional product either works or has a bug. An AI product is *probabilistic* — confident sometimes, uncertain other times, occasionally just wrong. The CPO designs for that: What does the user see when the AI isn't sure? What's the graceful failure? This is the single biggest difference between a CPO for an AI startup and a CPO for a normal one. (Anennya called this the "AI behavior card" in the May 5 brainstorm — it lives in `/cpo-requirements`.)

### Why the CPO is the "build the right thing" role

There's a classic distinction:
- The **CTO** makes sure you build the thing *right* (good engineering).
- The **CPO** makes sure you build the *right thing* (worth building at all).

You can have flawless engineering on a product nobody wants. The CPO exists to prevent that — the most expensive mistake in any product business.

---

## The PRD — What the CPO Workflow Produces

For a beginner building an app or workflow today, the destination artifact is a **PRD (Product Requirements Document)** — the spec you hand to your builder, whether that's a developer or Claude Code itself.

The CPO commands build up a PRD section by section:

```
A PRD =  the problem + user        (from /cpo-define)
       + what's in/out of v1       (from /cpo-scope)
       + what it must do, in detail (from /cpo-requirements)
       + how we'll measure success  (from /cpo-metrics)
```

The first four commands assemble into a complete PRD. The fifth (`/cpo-iterate`) is the loop you run *after* launch. We deliberately did NOT add a separate `/cpo-prd` assembly command — the PRD should fall out naturally as you run the steps, and `/cpo-metrics` ends by presenting the complete, build-ready PRD.

---

## Reconciling With Anennya's May 5 Design

Anennya already sketched the CPO workflow in the May 5 brainstorm with 5 commands. This doc keeps her structure and adds the evergreen frameworks underneath each, with one rename for beginner-friendliness:

| Anennya's name (May 5) | This doc | Change |
|---|---|---|
| `/cpo-define` | `/cpo-define` | unchanged |
| `/cpo-scope` | `/cpo-scope` | unchanged |
| `/cpo-stories` | `/cpo-requirements` | **renamed** — "stories" is jargon; "requirements" is plain English |
| `/cpo-metrics` | `/cpo-metrics` | unchanged |
| `/cpo-iterate` | `/cpo-iterate` | unchanged |

Her AI-specific "AI behavior cards" concept is preserved and lives inside `/cpo-requirements`.

---

## The Recommended Evergreen Frameworks

### 1. Jobs to Be Done (JTBD) ★ (Shared with CEO — the foundation)

**Source:** Clayton Christensen, *Competing Against Luck* (2016).

**What it is:** "People don't buy products; they hire them to do a job." The CPO inherits the Job Statement from the CEO's `/ceo-job` and uses it as the north star for what to build. Format: *"When [situation], I want to [motivation], so I can [expected outcome]."*

**Why it fits:** Keeps the product anchored to a real human need rather than a feature wishlist. The same JTBD that grounds CEO strategy grounds product definition — continuity across the org.

**How it powers a command:** Backbone of `/cpo-define` — the product definition is built directly on the job the user is hiring it to do.

---

### 2. Marty Cagan's "Inspired" — Valuable/Usable/Feasible/Viable ★ (The product test)

**Source:** Marty Cagan, *Inspired: How to Create Tech Products Customers Love* (2nd ed., 2017) and *Empowered* (2020). Cagan/SVPG is the most influential modern product-management voice.

**What it is:** Every product idea must pass four risk tests: **Valuable** (will people want it?), **Usable** (can they figure it out?), **Feasible** (can we build it?), **Viable** (does it work for the business?). Cagan's core principle: build to solve *problems*, not to ship *features*.

**Why it fits:** Gives beginners a simple four-question filter for every feature idea. It's the antidote to feature-list thinking. The "feasible" test is where CPO hands off to CTO; the "viable" test is where CPO checks back with CEO/CRO.

**How it powers a command:** Runs through `/cpo-define` (valuable + viable) and `/cpo-scope` (feasibility-aware cutting).

---

### 3. MoSCoW Prioritization + Shape Up "Appetite" ★ (How to scope the MVP)

**Source:** MoSCoW (Dai Clegg, 1994, DSDM method); Shape Up by Ryan Singer / Basecamp (2019).

**What it is:** Two complementary cutting tools:
- **MoSCoW** — sort every feature into Must-have / Should-have / Could-have / Won't-have. Forces explicit decisions about what's *not* in v1.
- **Shape Up "Appetite"** — instead of asking "how long will this take?", ask "how much time is this *worth*?" Set a fixed time budget (e.g. "this is a 2-week idea") and shape the solution to fit it. Flips estimation on its head.

**Why it fits:** Scoping is where most product projects die — from over-building. MoSCoW makes the cut explicit; appetite-framing stops the founder from gold-plating. Together they produce a tight, defensible MVP.

**How it powers a command:** Both run inside `/cpo-scope` — MoSCoW produces the feature list, appetite-framing sets the time budget.

---

### 4. User Stories + Acceptance Criteria + AI Behavior Cards ★ (Buildable requirements)

**Source:** User stories (Kent Beck / Mike Cohn, *User Stories Applied*, 2004); AI behavior cards (Anennya, May 5 brainstorm — original to this project).

**What it is:** Translate features into testable requirements:
- **User story format:** "As a [user], I want to [action], so that [outcome]."
- **Acceptance criteria:** how you know the story is done.
- **AI behavior card (AI-specific):** expected input, expected output, failure mode, and what the user sees when the AI is uncertain or wrong.

**Why it fits:** This is the bridge from "idea" to "buildable." The AI behavior card is the differentiated layer — it forces the founder to design the probabilistic, fails-sometimes nature of AI *before* building, not after a user complains.

**How it powers a command:** The core of `/cpo-requirements` — produces the requirements section of the PRD, including one AI behavior card per AI-powered feature.

---

### 5. North Star Metric + AARRR (Pirate Metrics) ★ (How to measure success)

**Source:** North Star Metric (Sean Ellis / Amplitude); AARRR (Dave McClure, 500 Startups — shared with CRO's growth work).

**What it is:**
- **North Star Metric** — the single number that best captures the value your product delivers to users (e.g. "reports generated per week per user"). Everything else is a supporting metric.
- **AARRR** — Acquisition → Activation → Retention → Referral → Revenue. The funnel that tells you *which part* of the product is working or broken. **Retention is the truth-teller** for product-market fit: do users come back without being prompted?

**Why it fits:** Beginners measure vanity metrics (signups, page views). North Star + AARRR forces them to measure value and retention — the only signals that matter early. Pairs with the Sean Ellis / Superhuman "very disappointed" test already noted in Phase 1's apps-track research.

**How it powers a command:** `/cpo-metrics` produces the North Star + 3-5 supporting KPIs mapped to AARRR + 30/60/90-day benchmarks.

---

### 6. Continuous Discovery — Opportunity Solution Tree ★ (The post-launch loop)

**Source:** Teresa Torres, *Continuous Discovery Habits* (2021). The modern standard for ongoing product discovery.

**What it is:** After launch, keep a steady habit of talking to users and mapping what you learn onto an **Opportunity Solution Tree**: the desired outcome at the root → customer opportunities (needs, pains, desires) as branches → possible solutions as leaves. It keeps "what to build next" tied to "why" — driven by real user evidence, not the loudest request.

**Why it fits:** Phase 1's apps-track research is explicit: *product-market fit is not a milestone, it's a loop.* Continuous Discovery is the disciplined version of that loop. It stops the founder from building based on the last thing a user said and instead builds from patterns.

**How it powers a command:** Backbone of `/cpo-iterate` — synthesizes feedback into an opportunity map and a prioritized "what's next" list for the following cycle.

---

## What's Intentionally Left Out (And Why)

| Framework | Why we're skipping it |
|---|---|
| **Full Scrum / SAFe** | Team-scale agile ceremony. Massive overkill for a solo or tiny founder. Shape Up's appetite model is the lighter, better fit. |
| **RICE / weighted scoring** | Useful once you have a big backlog and a team to align. Premature for an MVP — MoSCoW is enough. |
| **Kano Model** | Elegant for prioritizing delight vs. basics, but an extra layer most beginners don't need yet. Add later. |
| **Story points / velocity** | Estimation theater for solo builders. Appetite ("how much is this worth?") replaces it. |
| **Double Diamond (design)** | Lives better in the CDO/design role than CPO. |
| **Product Vision Board** | Mostly redundant once `/ceo-strategy` + `/cpo-define` are done. |

---

## The 5 CPO Sub-Commands — Beginner Question Naming

| Command | Beginner's Question | Framework underneath | PRD section |
|---|---|---|---|
| **`/cpo-define`** | "What am I building, and who's it for?" | JTBD + Cagan (Valuable/Viable) | Problem + user + core use case |
| **`/cpo-scope`** | "What goes into version 1 — and what doesn't?" | MoSCoW + Shape Up Appetite | In-scope / out-of-scope for v1 |
| **`/cpo-requirements`** | "What exactly must it do?" | User Stories + Acceptance Criteria + AI Behavior Cards | Detailed requirements |
| **`/cpo-metrics`** | "How will I know it's working?" | North Star + AARRR | Success metrics + 30/60/90 benchmarks |
| **`/cpo-iterate`** | "What do I build next?" | Continuous Discovery / Opportunity Solution Tree | *(post-launch loop — not part of initial PRD)* |

**Reads as a sentence:** *Define the product → scope v1 → write the requirements → set the metrics → iterate after launch.*

---

## How to Actually Run Them — The Step-by-Step Sequence

```
BUILD-READY PRD (run in order, produces the PRD you hand to your builder)
   /cpo-define       →  the problem + user + core use case
   /cpo-scope        →  what's in v1, what's out
   /cpo-requirements →  exactly what it must do (+ AI behavior cards)
   /cpo-metrics      →  how you'll measure success
        ↓
        →  Complete PRD → hand to CTO / developer / Claude Code to build
        ↓
POST-LAUNCH LOOP (run repeatedly after real users touch it)
   /cpo-iterate      →  feedback → opportunity map → next cycle's priorities
                          ↑___________ loops back to /cpo-scope _________|
```

**The first four are sequential and front-loaded. The fifth is a loop** — every feature cycle after launch starts with `/cpo-iterate`, which feeds an updated `/cpo-scope`.

---

## Connection to Other C-Suite Workflows

- **CEO → CPO:** The Job Statement from `/ceo-job` is the foundation of `/cpo-define`. The CEO's niche/ICP defines who the product is for.
- **CPO → CTO:** The PRD (especially `/cpo-requirements` + AI behavior cards) is the direct input to the CTO's build work (`/cto-mvp`, `/cto-sprint`). The "feasible" risk test is the CPO→CTO handoff.
- **CPO → CDO (Design):** User personas from `/cpo-define` feed `/design-user`; requirements from `/cpo-requirements` feed `/design-flows`.
- **CPO → CRO:** Pricing/packaging constraints from `/cro-pricing` set the scope boundaries `/cpo-scope` must fit within. The product's value proposition feeds the offer.
- **CPO → CMO:** The "who cares a lot" from `/cmo-positioning` validates or challenges the user personas in `/cpo-define`.

---

## Connections — The `/launch` Convergence Command

When `/launch` runs (for an apps/workflows business), it pulls these CPO artifacts:

| CPO command output | What `/launch` uses it for |
|---|---|
| `/cpo-define` → product definition | Confirms what's being launched matches the strategic bet |
| `/cpo-scope` → MVP scope | Launch readiness gate: is the product actually shippable? |
| `/cpo-metrics` → North Star + benchmarks | The success criteria the launch will be measured against (feeds AARRR in `/launch`) |
| `/cpo-requirements` → AI behavior cards | Confirms graceful-failure behavior is built before real users hit it |

CPO answers the "is the product ready?" gate in the Launch Readiness Checklist — one of the four convergence inputs (alongside CEO segment, CMO message, CRO pricing).

---

## Triggers and Trigger Re-Entry

### When the FULL CPO sequence runs

| Trigger | What just happened | Why the full sequence runs |
|---|---|---|
| **New product / app** | Founder starting an apps/workflows build from zero | Need define → scope → requirements → metrics → (then build) |
| **Major pivot** | `/ceo-pivot` declared | The product bet changed; PRD must be rebuilt from `/cpo-define` |
| **New product line** | Adding a second product to the business | Each product needs its own PRD |

### When a SUBSET re-fires

| Trigger | What just happened | Commands that re-fire | Why |
|---|---|---|---|
| **Building a new feature** | Adding to an existing product | `/cpo-scope` (scoped to the feature) → `/cpo-requirements` | New scope + requirements; define already exists |
| **Users aren't activating** | Signups but no real usage | `/cpo-define` (wrong user/job?) + `/cpo-metrics` (measuring the wrong thing?) | Activation gap signals a definition or metric problem |
| **Scope is ballooning** | The build is taking far longer than expected | `/cpo-scope` (re-cut with MoSCoW + appetite) | Classic over-build — re-scope hard |
| **Feedback is piling up** | Lots of user requests post-launch | `/cpo-iterate` | The post-launch loop — synthesize before building |
| **AI keeps failing in a confusing way** | Users hit AI errors with no guidance | `/cpo-requirements` (fix the AI behavior cards) | Graceful-failure design gap |
| **Can't tell if it's working** | No clear signal of success | `/cpo-metrics` (set a real North Star) | Measurement gap |
| **Quarterly review** | End of OKR cycle | `/cpo-metrics` (review against benchmarks) + `/cpo-iterate` | Periodic product health check |

### Convergence triggers

| Trigger | Commands across roles |
|---|---|
| **Go-to-market launch** | `/cpo-scope` + `/cpo-metrics` locked → product-readiness gate for `/launch` |
| **Feature launch** | `/cpo-scope` + `/cpo-requirements` → CTO build → CMO announce → CRO price |
| **Pivot decision** | `/ceo-pivot` → `/cpo-define` (reset) → full PRD rebuild |
| **First hire (e.g. a developer)** | `/cpo-requirements` (the spec they build from) + CTO onboarding |

---

## Open Questions / Next Steps

- [ ] Validate with Patty and Anennya — especially the `/cpo-stories` → `/cpo-requirements` rename
- [ ] Confirm the PRD-as-natural-output approach (vs. an explicit `/cpo-prd` assembly command)
- [ ] Design the consulting-lite path for a later iteration (productized-service definition without full software PRD)
- [ ] Decide how `/cpo-requirements` hands the PRD to Claude Code specifically — is there a "build this" handoff format?
- [ ] Move on to **CTO** next — reconcile with Anennya's May 5 design (`/cto-stack`, `/cto-architecture`, `/cto-mvp`, `/cto-sprint`, `/cto-ship`, `/cto-ai`, `/cto-review`). Candidate frameworks: decision-vs-build modes, ADRs (Architecture Decision Records), Wizard of Oz MVP, the build-vs-buy decision, LLM selection / eval frameworks.

---

## Sources

- Christensen, C.M. et al. *Competing Against Luck: The Story of Innovation and Customer Choice*. Harper Business, 2016.
- Cagan, M. *Inspired: How to Create Tech Products Customers Love* (2nd ed.). Wiley, 2017. / *Empowered*. Wiley, 2020. [SVPG — Empowered Product Teams](https://www.svpg.com/empowered-product-teams/)
- Clegg, D. & Barker, R. *Case Method Fast-Track: A RAD Approach* (MoSCoW). Addison-Wesley, 1994.
- Singer, R. *Shape Up: Stop Running in Circles and Ship Work that Matters*. Basecamp, 2019. https://basecamp.com/shapeup
- Cohn, M. *User Stories Applied: For Agile Software Development*. Addison-Wesley, 2004.
- Ellis, S. & Brown, M. *Hacking Growth* (North Star Metric). Currency, 2017.
- Torres, T. *Continuous Discovery Habits*. Product Talk LLC, 2021. [Opportunity Solution Trees](https://www.producttalk.org/opportunity-solution-trees/)
- O'Brien Novak, P. *Phase-1-Frameworks-Patty.md* (WDAI repo, April 2026). / Anennya, *2026_05_05_Brainstorming_C_Suite.md* (WDAI repo).
