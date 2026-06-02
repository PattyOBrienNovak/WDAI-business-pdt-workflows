# CTO Frameworks — Evergreen Best Practices

**Session with Claude Code — May 12, 2026**
*Participant: Aparna*
*Purpose: Identify the evergreen, best-practice frameworks the CTO (Chief Technology Officer) role should draw from, sourced from established engineering thought leadership and current AI-engineering practice. Reconciles with Anennya's May 5 CTO command design (decision mode vs. build mode). Command naming follows a beginner-friendly logic.*

> **Scope note:** Like CPO, the CTO role is built for the **apps and workflows tracks**. Pure consultants don't need it (unless they're building tooling to deliver their service). The role is designed to work in **two modes** — Decision mode for non-technical founders, Build mode for technical founders — so it serves the full WDAI spectrum.

---

## How a CTO Operates — Explained to a Beginner Founder

**The one-line version:** The CTO decides *what you build with* and *makes sure it actually works and stays up.* If the CPO decides what to build, the CTO decides how it gets built — and for a non-technical founder, that mostly means making good technology *decisions*, not writing code.

### The two modes (the key idea — from Anennya's May 5 design)

This is the most important thing about the CTO role for WDAI:

- **Decision mode** — for the non-technical founder who needs to *understand and approve* technology choices without writing code. "Should I use this tool or that one? Should I build this or buy it? Which AI model for which task?" The output is a confident decision with plain-English rationale.
- **Build mode** — for the technical founder (or once a developer joins) who is actually *implementing*. The output is engineering scope, build order, and shipping process.

Every CTO command works in both modes. A non-technical founder lives mostly in Decision mode and hands Build mode to a developer or to Claude Code. A technical founder uses both.

### The four things every CTO really does

1. **Chooses the tools.** Decides the technology stack — what you build with — based on the team's skills, budget, and how much it needs to scale. For AI products, this includes *which AI model for which task.*
2. **Designs how the pieces fit.** Decides how the parts of the system connect — where data lives, where AI calls happen, what must never break.
3. **Builds in the right order.** Decides what to build first, what can be faked manually before automating, and what to cut if behind schedule.
4. **Ships and keeps it running.** Gets it live safely, watches it after launch, and has a plan for when something breaks.

### The mindset shift that defines the role

The single most useful principle for a beginner CTO is **"Choose Boring Technology"** (Dan McKinley): you get a limited number of "innovation tokens." Spend them on the *one* thing that makes your product special (for you, that's the AI) — and use boring, proven, well-documented tools for everything else (auth, payments, hosting, database). Boring technology has known failure modes and tons of help available when you get stuck. New-and-shiny does not.

The second reframe, unique to AI products: **the AI is the riskiest part, so design it last and test it hardest.** A non-AI feature either works or has a bug. An AI feature is probabilistic — you have to *evaluate* it, not just test it. In 2026, "evals" went from a research nicety to a production gate. The CTO's job is to know how good is good enough, and how to measure it.

### Why the CTO is the "build it right" role

Recall the CPO vs. CTO split:
- The **CPO** makes sure you build the *right thing* (worth building).
- The **CTO** makes sure you build the thing *right* (works, scales enough, stays up).

For a non-technical founder, the CTO role is mostly about *not getting taken advantage of* — making informed technology decisions so you don't overpay, over-build, or get locked into the wrong tool. It demystifies the technical layer so you stay in control.

---

## Reconciling With Anennya's May 5 Design

Anennya designed 7 CTO commands in the May 5 brainstorm, including the two-mode concept and the AI-specific command. This doc keeps all 7 and adds evergreen frameworks underneath each. Names are kept close to hers to honor the original design; beginner-question framing is layered on top.

| Anennya's command (May 5) | Mode | Kept as |
|---|---|---|
| `/cto-stack` | Decision | `/cto-stack` |
| `/cto-architecture` | Decision | `/cto-architecture` |
| `/cto-mvp` | Decision → Build | `/cto-mvp` |
| `/cto-sprint` | Build | `/cto-sprint` |
| `/cto-ship` | Build | `/cto-ship` |
| `/cto-ai` ★ | Both | `/cto-ai` |
| `/cto-review` | Build (advanced) | `/cto-review` |

`/cto-ai` is the differentiated command — it has no equivalent in a traditional startup toolkit.

---

## The Recommended Evergreen Frameworks

### 1. Choose Boring Technology + Build vs. Buy ★ (How to pick the stack)

**Source:** Dan McKinley, *Choose Boring Technology* (2015) — the "innovation tokens" essay; plus the classic Build-vs-Buy decision discipline.

**What it is:** You have a limited number of innovation tokens. Spend them on what makes your product special; use boring, proven tech for everything else. And before building anything, ask: *can I buy/use something that already exists?* At MVP stage, buy/integrate almost always beats build.

**Why it fits:** Non-technical founders are the most vulnerable to shiny-tech advice and to "we should build our own X." This framework gives them a defensible default: boring everything except the AI, and don't build what you can rent. Saves money, time, and lock-in.

**How it powers a command:** Backbone of `/cto-stack` — produces a recommended stack with plain-English rationale, cost estimate, and "what's easy vs. hard to change later." For AI specifically: API vs. self-hosted, and "don't fine-tune at MVP stage."

---

### 2. Architecture Decision Records (ADRs) ★ (How to document the "why")

**Source:** Michael Nygard, *Documenting Architecture Decisions* (2011). Now an industry-standard lightweight practice.

**What it is:** A short doc per significant decision: what we decided, why, what we considered, and what the trade-offs are. Cheap to write, invaluable later when you (or a new developer) ask "why did we do it this way?"

**Why it fits:** A non-technical founder making technology decisions needs a paper trail they actually understand. ADRs turn invisible technical choices into plain-English records the founder owns — and that a future developer can pick up without re-litigating everything.

**How it powers a command:** Built into `/cto-architecture` — every key decision is captured in ADR format (plain-English: decided / why / considered / trade-off).

---

### 3. Wizard of Oz / Concierge MVP ★ (How to fake it before you build it)

**Source:** Lean Startup (Eric Ries) — Wizard of Oz and Concierge MVP patterns. Already echoed in Anennya's May 5 "fake it" principle.

**What it is:** Before automating something expensive, do it manually behind the scenes so it *looks* automated to the user. "Wizard of Oz" = a human pulls the levers the user thinks software is pulling. Lets you validate demand before building the hard part.

**Why it fits:** This is the single biggest cost-saver for an early product. For AI especially — before building a complex pipeline, a human (or you + Claude) can produce the output manually and confirm people want it. Extends the MVP principle into engineering.

**How it powers a command:** Core of `/cto-mvp` — for each feature, produces a "fake it" option (what a human can do manually first) alongside the real build estimate and dependency-ordered build plan.

---

### 4. Lightweight Weekly Planning (Appetite-based) (How to decide what to build this week)

**Source:** Shape Up appetite framing (Basecamp — shared with CPO); adapted to solo/tiny-team cadence.

**What it is:** Instead of heavy sprint ceremony, a simple weekly question: what's the one goal this week, what are the tasks, what's blocking me, and what's the time budget? For solo founders it's a weekly priority list, not a sprint ritual.

**Why it fits:** Beginners either over-plan (full Scrum for a one-person team) or don't plan at all. A lightweight weekly cadence is the right middle. Pairs with the CPO's scope work — this is where "what's in v1" becomes "what I do this week."

**How it powers a command:** `/cto-sprint` — produces a one-sentence weekly goal + task list + blockers + dependencies (what needs design or CPO sign-off first). Build mode; for solo founders it's a weekly plan, not a sprint.

---

### 5. Pre-Launch Checklist + Rollback + Monitoring ★ (How to ship safely)

**Source:** Site Reliability Engineering practice (Google SRE); Gawande's Checklist Manifesto (shared with COO); plus an AI-specific launch checklist.

**What it is:** A pre-launch checklist (env vars set, error monitoring live, AI rate limits + cost alerts configured, fallback behavior defined), deployment steps, post-launch health checks (what to watch in the first 30 min), and a rollback plan for when it breaks.

**Why it fits:** Shipping is where non-technical founders feel most exposed. A checklist turns "I hope this works" into "I followed the steps." The **AI-specific items** (rate limits, cost alerts, fallback when the LLM call fails, latency baseline) are the differentiator — these are exactly the things that blow up an AI product at launch and that no generic checklist covers.

**How it powers a command:** `/cto-ship` — produces the pre-launch checklist (with AI-specific items), deployment steps, health checks, rollback procedure, and a launch signal to CMO/CPO.

---

### 6. AI Engineering — Model Selection + Evals + Prompt Management ★★ (The differentiated command)

**Source:** Current AI-engineering practice (2026): eval-driven development (Define → Test → Diagnose → Fix), model selection per task, prompt versioning, RAG evaluation (faithfulness, context precision). Tools like Promptfoo (model/prompt comparison), DeepEval/RAGAS (RAG metrics).

**What it is:** The decisions that make AI features actually reliable:
- **Model selection per task** — reasoning vs. speed vs. cost; which model for which job.
- **Prompt management** — where prompts live, how they're versioned, how they're tested.
- **Evaluation framework** — how you measure output quality (deterministic checks, LLM-as-judge, or human eval). In 2026, **evals are a production gate, not a checkbox.**
- **RAG decision** — do you need retrieval at all? What goes in the vector store?
- **Cost monitoring** — token costs can silently balloon; set alerts.

**Why it fits:** This is the bridge between the CPO's "AI behavior cards" and actual implementation. It's the most differentiated part of the entire toolkit — no traditional startup playbook has it, and it's directly relevant to everything the WDAI community builds.

**How it powers a command:** `/cto-ai` — produces model selection per task (with cost/latency trade-offs), a prompt management strategy, an evaluation plan, the RAG decision, and cost-monitoring setup. Works in both modes: Decision mode for "which model + do I need RAG," Build mode for "here's how to wire up evals."

---

### 7. Technical Debt Register + Theory of Constraints (Advanced — what to fix next)

**Source:** Ward Cunningham's technical debt metaphor; Goldratt's Theory of Constraints (shared with COO).

**What it is:** A register of what's slowing you down (what it is, why it matters, effort to fix), prioritized by the *one* constraint currently limiting progress. Decide what to refactor vs. rebuild vs. leave alone.

**Why it fits:** Mostly relevant once a product is live and accumulating cruft. The Theory of Constraints lens stops founders from polishing the wrong thing — fix the one bottleneck, not the most annoying thing.

**How it powers a command:** `/cto-review` (advanced) — produces a tech debt register + prioritized fix list focused on the current bottleneck.

---

## What's Intentionally Left Out (And Why)

| Framework | Why we're skipping it |
|---|---|
| **Microservices / distributed systems patterns** | Wildly premature for an MVP. "Boring monolith" is the right early answer. Add never, probably. |
| **Full DevOps / Kubernetes / IaC** | Enterprise-scale operations. A managed platform (Vercel, Railway, Supabase) is the right call for this audience. |
| **Full Scrum / SAFe** | Team-scale ceremony. The lightweight weekly cadence replaces it. |
| **Design patterns / SOLID deep-dives** | Build-mode implementation detail. Claude Code handles most of this; not a founder-decision framework. |
| **Fine-tuning / custom model training** | Almost never worth it at MVP stage (noted explicitly in `/cto-stack`). API-first is the default. |

---

## The 7 CTO Sub-Commands — Beginner Question Naming

| Command | Beginner's Question | Mode | Framework underneath |
|---|---|---|---|
| **`/cto-stack`** | "What should I build this with?" | Decision | Choose Boring Technology + Build vs. Buy |
| **`/cto-architecture`** | "How do the pieces fit together?" | Decision | Architecture Decision Records (ADRs) |
| **`/cto-mvp`** | "What do I build first (and what can I fake)?" | Decision → Build | Wizard of Oz / Concierge MVP |
| **`/cto-sprint`** | "What do I work on this week?" | Build | Lightweight weekly planning (appetite) |
| **`/cto-ship`** | "How do I launch it safely?" | Build | Pre-launch checklist + rollback + monitoring |
| **`/cto-ai`** ★ | "How do I make the AI part actually reliable?" | Both | Model selection + evals + prompt management |
| **`/cto-review`** *(advanced)* | "What's slowing me down, and what do I fix next?" | Build | Tech debt register + Theory of Constraints |

**Reads as a sentence:** *Pick your tools → design how it fits → decide what to build first → plan the week → make the AI reliable → ship it safely → fix what slows you down.*

---

## How to Actually Run Them — The Step-by-Step Sequence

```
DECISION MODE (do first — non-technical founders can stop here and hand off)
   /cto-stack        →  what to build with (boring everything except AI)
   /cto-architecture →  how the pieces fit (captured as ADRs)
   /cto-ai           →  model selection + eval plan (the AI decisions)
   /cto-mvp          →  build order + what to fake first

BUILD MODE (when actually implementing — you, a dev, or Claude Code)
   /cto-sprint       →  weekly goal + tasks (repeat each week)
   /cto-ship         →  launch safely with the checklist
        ↓
ADVANCED (once it's live and accumulating cruft)
   /cto-review       →  fix the one bottleneck slowing you down
```

**Decision mode is front-loaded and accessible to non-technical founders.** Build mode is where implementation happens — handed to a developer or Claude Code if the founder doesn't code. `/cto-ai` deliberately sits in Decision mode because the *choices* (which model, do I need RAG, how good is good enough) must be made before building, even by a non-technical founder.

---

## The MVP Boundary — CPO vs. CTO

Both roles have an "MVP" step, but they're different:

| | `/cpo-scope` (CPO) | `/cto-mvp` (CTO) |
|---|---|---|
| **Question** | What features are in v1? | In what order do we build them, and what can we fake? |
| **Lens** | Product value (MoSCoW, appetite) | Engineering feasibility + build order + Wizard of Oz |
| **Output** | MVP feature list (the "what") | Build plan + dependency chain + fake-it options (the "how") |

`/cpo-scope` decides *what's worth building*; `/cto-mvp` decides *how to build it in the smartest order*. CPO hands its scope to CTO.

---

## Connection to Other C-Suite Workflows

- **CPO → CTO:** The PRD from `/cpo-requirements` (with AI behavior cards) is the direct input to `/cto-mvp` and `/cto-ai`. The "feasible" risk test is the CPO→CTO handoff.
- **CTO → CDO (Design):** The stack/framework choice from `/cto-stack` affects which component library Design can use; the API surface from `/cto-architecture` informs what's possible in `/design-flows`.
- **CTO → CMO:** The launch signal from `/cto-ship` triggers the CMO's announcement (`/cmo-content`).
- **CTO → CPO:** Technical constraints surfaced in `/cto-stack` and `/cto-architecture` feed back to `/cpo-scope` (what's expensive vs. cheap to build).
- **CTO ↔ COO:** Cost monitoring (`/cto-ai`) and the operations stack (`/coo-stack`) overlap — AI API costs are an operating expense.

---

## Connections — The `/launch` Convergence Command

When `/launch` runs (apps/workflows), it pulls these CTO artifacts:

| CTO command output | What `/launch` uses it for |
|---|---|
| `/cto-ship` → pre-launch checklist | The technical half of the Launch Readiness Checklist |
| `/cto-ai` → eval results | Launch gate: is the AI good enough to put in front of users? |
| `/cto-architecture` → cost estimate | Confirms the unit economics work before scaling traffic |
| `/cto-mvp` → build status | Confirms the product is actually built and shippable |

CTO provides the **technical-readiness gate** in `/launch` — the AI eval pass/fail is a hard gate (don't launch an AI product that fails its own evals).

---

## Triggers and Trigger Re-Entry

### When the FULL CTO sequence runs

| Trigger | What just happened | Why the full sequence runs |
|---|---|---|
| **New product / app** | Starting an apps/workflows build | Need stack → architecture → AI decisions → MVP → sprint → ship |
| **Major pivot** | `/ceo-pivot` declared | Tech choices may change; re-run from `/cto-stack` (what carries over?) |
| **Rebuild / re-platform** | Outgrew the MVP stack | Full re-evaluation of stack and architecture |

### When a SUBSET re-fires

| Trigger | What just happened | Commands that re-fire | Why |
|---|---|---|---|
| **Building a new feature** | Adding to existing product | `/cto-mvp` (feature) → `/cto-sprint` → `/cto-ship` | Scope the feature build; stack already chosen |
| **AI output quality is poor** | Users getting bad/wrong AI results | `/cto-ai` (re-run evals, change model/prompt) | The eval-driven loop: Define → Test → Diagnose → Fix |
| **AI costs are ballooning** | Token bill is surprisingly high | `/cto-ai` (cost monitoring + model selection) | Wrong model for the task, or no cost controls |
| **Something broke in production** | Outage or major bug | `/cto-ship` (rollback) + `/investigate`-style root cause | Need the rollback plan + debugging |
| **Shipping feels scary/manual** | Deploys are error-prone | `/cto-ship` (formalize the checklist) | Reliability gap |
| **Everything feels slow to build** | Velocity dropping | `/cto-review` (find the bottleneck) | Tech debt is accumulating |
| **A developer is joining** | First technical hire | `/cto-architecture` (ADRs as onboarding doc) | The ADRs are the handoff doc |
| **Quarterly review** | End of OKR cycle | `/cto-review` + `/cto-ai` (eval health) | Periodic technical health check |

### Convergence triggers

| Trigger | Commands across roles |
|---|---|
| **Go-to-market launch** | `/cto-ship` + `/cto-ai` (evals pass) → technical-readiness gate for `/launch` |
| **Feature launch** | `/cpo-requirements` → `/cto-mvp` → `/cto-sprint` → `/cto-ship` → CMO announce |
| **Pivot decision** | `/ceo-pivot` → `/cto-architecture` (what carries over?) → `/cto-mvp` (new) |
| **First technical hire** | `/cto-architecture` (onboarding) + `/cpo-requirements` (the spec) |

---

## Open Questions / Next Steps

- [ ] Validate with Patty and Anennya — especially keeping all 7 commands vs. trimming for the non-technical majority
- [ ] Should the most jargony names be renamed for beginners? (`/cto-sprint` → `/cto-weekly`, `/cto-review` → `/cto-cleanup`, `/cto-mvp` → `/cto-buildplan`?) Kept Anennya's names for now to honor the original design.
- [ ] Define the explicit "hand this to Claude Code to build" format — the bridge from `/cto-mvp` build plan to actual implementation
- [ ] Decide how deep `/cto-ai` goes for a true non-technical founder vs. a build-mode founder (two output depths?)
- [ ] Move on to the final role, **CDO (Design)** — reconcile with Anennya's May 5 design (`/design-brand`, `/design-user`, `/design-flows`, `/design-system`, `/design-test`). Confirm the `/cmo-brandidentity` (strategy) vs. `/design-brand` (execution) boundary. Candidate frameworks: Double Diamond, Design Thinking (IDEO), Nielsen's usability heuristics, Jobs to Be Done for UX, atomic design.
- [ ] After CDO: spec the top-level `/launch` convergence command (all 7 roles will be defined).

---

## Sources

- McKinley, D. ["Choose Boring Technology"](https://mcfunley.com/choose-boring-technology). 2015.
- Nygard, M. ["Documenting Architecture Decisions"](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions). 2011.
- Ries, E. *The Lean Startup*. Crown Business, 2011. (Wizard of Oz / Concierge MVP.)
- Singer, R. *Shape Up*. Basecamp, 2019. (Appetite-based planning.)
- Beyer, B. et al. *Site Reliability Engineering*. O'Reilly / Google, 2016.
- Gawande, A. *The Checklist Manifesto*. Metropolitan Books, 2009.
- Cunningham, W. The technical debt metaphor (1992 OOPSLA experience report).
- Goldratt, E.M. *The Goal*. North River Press, 1984. (Theory of Constraints.)
- [LLM Evaluation Frameworks & best practices for 2026 — MLAI Digital](https://www.mlaidigital.com/blogs/llm-model-evaluation-frameworks-a-complete-guide-for-2026); ["When Better Prompts Hurt: Evaluation-Driven Iteration for LLM Applications" (arXiv, 2026)](https://arxiv.org/pdf/2601.22025)
- Anennya, *2026_05_05_Brainstorming_C_Suite.md* (WDAI repo).
