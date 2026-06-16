# Audience and MVP — June 3, 2026

*Drafted from pre-meeting discussion between Anennya and Claude Code.*

---

## The Audience

### What this toolkit is

This is the product — not a demo, not a workshop tool. It gives anyone building an AI business a structured, automated path through the work. The value scales with what you bring: a first-timer gets the framework plus the output; an experienced PM skips the learning and gets speed and structure.

**Prerequisite: Claude Code fluency.** Users need to be comfortable running slash commands in a CLI. This is not a beginner experience and doesn't need to be — WDAI is increasingly adopting Claude Code and that adoption is the entry point.

---

### The three real segments

**1. WDAI members building their first AI business**
Know their domain (HR, finance, healthcare, marketing, etc.), new to the business and product frameworks. The commands teach and produce at the same time — they learn positioning by doing it, not by reading about it. The output is professional even without prior expertise.

**2. Experienced PMs, marketers, and founders**
Already know what a PRD is, already know about positioning. The value is speed and connective tissue — running `/cpo-define` through `/cpo-metrics` produces a build-ready PRD in 30 minutes instead of 3 hours. Their JTBD automatically seeds their requirements; their positioning automatically seeds their pitch. No manual context porting between documents.

**3. Solopreneurs with a product idea**
Have domain knowledge and an idea, missing the structured path from idea to shipped product. The CPO/CTO block is exactly their gap — especially `/cto-ai`, which is genuinely novel even for experienced people.

---

### The unifying characteristic

> **Claude Code users building something in the AI space who want the work to go faster and be more structured.**

---

## The MVP

### Infrastructure (must exist first)

| Piece | What it does |
|---|---|
| **Shared business brief** | The backbone — every command reads from and writes to it. Without it you have prompts, not a system. Holds: JTBD, product definition, MVP scope, stack choice, AI model decisions, track, `founder_technical` flag. |
| **`/start`** | The routing front door — 2-3 questions, routes to the right first command. Detects if a brief already exists for returning users. |

---

### The 8 commands: idea → shipped product

**Foundation**

| Command | What it does | Writes to brief |
|---|---|---|
| `/ceo-define-problem` | JTBD — who hires this product and for what. 10-minute exercise that unlocks everything downstream. | niche, ICP, job statement |

**The PRD block**

| Command | What it does | Writes to brief |
|---|---|---|
| `/cpo-define` | Product definition — reads JTBD from brief, adds user + core problem | product definition |
| `/cpo-scope` | MVP cut — what's in v1 and explicitly what's NOT (MoSCoW + appetite framing) | MVP scope |
| `/cpo-requirements` | What it must do + **AI behavior cards** (expected input/output, failure modes, graceful degradation) | requirements |

**The build block**

| Command | What it does | Writes to brief |
|---|---|---|
| `/cto-stack` | What to build with — boring everything except the AI; build vs. buy decisions | stack choice |
| `/cto-ai` | Model selection + evals + prompt management — **the differentiator** | AI decisions |
| `/cto-mvp` | Build order + what to fake first (Wizard of Oz / Concierge MVP) | build plan |
| `/cto-ship` | Pre-launch checklist + rollback + AI-specific monitoring | ship status |

---

### Why these 8

The end-to-end journey is complete: a solopreneur runs `/start` and walks away with a PRD they can hand to a developer or Claude Code, a build plan with the right stack and AI decisions, and a safe ship process. Everything connects through the brief — JTBD seeds the product definition, scope constrains the requirements, stack choice informs the build order.

**`/cto-ai` is the differentiator.** No other toolkit tells a solopreneur which model to use, how to set up evals, and how to design for when the AI is wrong. That's the command experienced PMs don't have elsewhere either.

**`/ceo-define-problem` is the lightest possible CEO footprint** — one JTBD statement that takes 10 minutes and unlocks everything downstream. The full strategy cascade (Playing to Win, Hedgehog, OKRs) is deferred until phase 2.

---

### The test for "MVP is working"

A solopreneur with an idea runs through all 8 commands and ends up with:

1. A complete PRD with AI behavior cards — ready to hand to a developer or Claude Code
2. A build plan with stack, model choices, and build order
3. A ship checklist ready to go

All connected through the brief. No blank pages. No re-explaining context between steps.

---

### Phase 2 — after the product is shipped

Once the product exists, the natural next need is "how do I talk about it and get users." The brief is already populated from phase 1, so these commands know the product without re-asking:

| Command | What it adds |
|---|---|
| `/cmo-positioning` | How to talk about the product — who it's for, why it's better than alternatives |
| `/cmo-messaging` | What to say — BrandScript as source for landing page, LinkedIn, pitch |
| `/cro-draft-offer` | What you're selling — turns the product into a concrete, priced thing |
| `/cro-outreach` | How to get first users — warm contacts, beachhead outreach |
| `/design-brand` | Visual identity (useful across all tracks) |
| `/design-flows` | Core user flows — before handing to CTO to build |
| `/launch` | GTM convergence — pulls from CMO + CRO + CPO + CTO to produce a launch plan |

---

### What's deferred to phase 3

- Full CEO sequence (strategy, hedgehog, assumptions, OKRs, validate, pivot)
- Full CMO sequence (credibility, audience, content)
- Full CRO sequence (final offer, pricing, discovery, pitch, grow)
- Full COO sequence (setup, contracts, scope, deliver, getpaid, systemize)
- Full CDO sequence (user research, design system, usability testing)
- Advanced commands: `/cto-review`, `/cto-sprint`, `/coo-systemize`
