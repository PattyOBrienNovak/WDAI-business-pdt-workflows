# Brainstorming for Starting an AI Business
**Session with Claude Code — April 10–13, 2026**
*Participants: Patty & Anennya*

---

## Claude Code Review — April 23, 2026

### What's Strong

**The lifecycle model is the core insight.** Mapping `/discover` through `/grow` as a business lifecycle — analogous to the dev lifecycle in the quickstart repo — is exactly the right structural choice. It gives people a clear path without forcing them to follow it linearly.

**Promotion as a thread, not a step.** This is probably the single best idea in the doc. Most business toolkits bolt marketing on at the end. Weaving "Now share it" into every command addresses the exact behavior gap your audience has — and it's a genuine differentiator.

**"Teaching along the way" design.** The one-sentence-before, one-line-after approach is smart. It respects people's time while still building understanding. The `/teach-me` command is a great safety valve for curiosity without cluttering the main flow.

**Build Hour format.** The 5-10-15-10 structure with member contributions folding back into the repo is a real flywheel — it produces the product, builds community, and generates testimonials simultaneously.

### Where to Push Back or Sharpen

**The 3 tracks may be too much to start.** Consulting, workflows, and apps are genuinely different businesses. Building all 3 tracks well is a large scope. Consider picking ONE track for the first Build Hour series (consulting is probably the most accessible for non-technical members), proving the model works, then expanding. The core lifecycle commands are track-agnostic anyway — the track folders are the variable part.

**The access model undersells the friction problem.** Even a private GitHub repo with Claude Code is a real barrier for non-technical business people. The doc acknowledges this ("Notion/PDF = friendly front door") but treats it as secondary. For your audience, it might need to be primary. Consider whether the first version should live entirely in a format your members already use (Notion, Google Docs) with GitHub as the backend your team manages.

**`/deliver` is doing too much work.** Delivering a consulting engagement vs. building an automation workflow vs. shipping an MVP app are fundamentally different. This command either needs to be track-specific from day one, or scoped to what's universal (client communication, milestone tracking, handoff).

**Missing: `/validate` before `/discover`.** Many people in your community probably have an idea but aren't sure if anyone will pay for it. A lightweight validation step — "describe your idea, let's find 3 signals that people want this" — could prevent weeks of wasted effort and would be a natural Build Hour 1 activity.

**Missing: money and legal basics.** There's no command for "how do I actually get paid" — invoicing, payment terms, LLC vs. sole proprietor, basic tax considerations. `/operate` mentions contracts and tools, but the financial plumbing of running a business is a common early blocker.

**The open questions are the real blockers.** The doc is ready to build from, but the launch date question drives everything. Resolve that first, then work backward to determine what must be ready by then.

### Bottom Line

This is a strong foundation — the lifecycle model, promotion-as-thread, and build-in-public strategy all reinforce each other well. The main risk is scope: trying to ship all 3 tracks and 7+ commands before you have real member feedback. Consider launching with the core lifecycle commands (track-agnostic), one track (consulting), and the first 3 commands (`/discover`, `/position`, `/price`) for Build Hour sessions 1-3. Let member usage tell you what to build next.

---

## The Idea

> **Patty:** Hey - Anennya and I want to create a repo similar to this one: https://github.com/anennya/claude-code-quickstart but for how to start an AI business whether it's consulting, creating workflows or developing apps. We figure there are many steps that are the same across any of these. We want to create this into something usable by our Women Defining AI community. But we don't have much experience with starting an AI business and need your help and guidance. That could be doing some research across reddit, X, Youtube, etc. Combing really popular github repos, etc. for the best grouping of skills and commands people could use to help them know what to do for their new business. We need guidance and a plan on how to go about this project. Ideally we want a plan so we can then create some of these workflows in public with our WDAI community. Ok, curious to hear your thoughts and plans...

---

## Understanding the Existing Repo

We started by reviewing `anennya/claude-code-quickstart`. Key findings:

- It's a **developer lifecycle SDK**: brainstorm → plan → build → audit → fix → ship
- Provides repeatable slash commands (`/brainstorm`, `/plan`, `/build`, `/closeout`, etc.)
- Skills folders deepen each command (TDD, UI development, debugging, observability)
- Value: you never start from scratch on a new project

The new repo should do the same thing — but for an **AI business lifecycle**, not a coding lifecycle.

---

## Initial Plan Proposed

### Phase 1: Research (suggested, then deferred)
Comb Reddit (r/AItools, r/freelance, r/Entrepreneur), popular GitHub repos, YouTube, and X/Twitter to find the 10–15 things everyone needs to figure out when starting an AI business — regardless of model (consulting, workflows, or apps).

### Phase 2: Structure the Lifecycle
Universal AI business lifecycle hypothesis:

```
/discover    → niche + ICP research, competitive landscape
/position    → messaging, offer definition, differentiation
/price       → pricing models (retainer, project, productized)
/pitch       → proposals, decks, outreach sequences
/deliver     → project/workflow/app delivery playbook
/operate     → client onboarding, contracts, tools stack
/grow        → case studies, referrals, upsells, community
```

With **track-specific branches** for:
- `consulting/` — discovery calls, scope docs, proposals
- `workflows/` — automation stack (n8n, Make, Zapier), client handoff
- `apps/` — MVP scoping, stack selection, go-to-market

### Phase 3: Build in Public with WDAI
Structure the repo so community members can:
1. **Use it** immediately with slash commands for their specific business
2. **Contribute** by adding their own templates, scripts, case studies
3. **Workshop it** — each section becomes a live session topic

---

## Clarifying Questions + Answers

> **Claude asked:**
> 1. Who is the target user exactly?
> 2. Which of the 3 tracks is most relevant to your community right now?
> 3. Do you want this as a fork/sister repo or standalone org under WDAI?
> 4. How public is "public"?

> **Patty answered:**
> 1. WDAI members who are business people but typically not technical.
> 2. All 3 tracks.
> 3. Standalone org under WDAI.
> 4. Gated to WDAI members for now. Eventually it may become a product we offer to the world for a price.

---

## Revised Plan: Non-Technical Business People First

This changes the design significantly from the existing repo. Key design principles:

- **Setup must be near-zero friction** — ideally just download and drag a file
- **Commands must speak business, not tech** — `/discover`, `/price`, `/pitch` not `/build`, `/audit`, `/fix`
- **Outputs are business artifacts** — proposals, pricing docs, client emails, contracts — not code
- **Claude Code as a business co-pilot**, not a coding assistant

This is actually more ambitious than Sandhya's repo because it's teaching people a new way to run their business, not just a new dev workflow.

---

## Proposed Repo Structure

```
wdai-ai-business-starter/
├── README.md                  ← welcoming, non-technical, clear value prop
├── SETUP.md                   ← 3-step setup, desktop app focused, no terminal required
├── CLAUDE.md                  ← business-focused instructions for Claude
│
├── .claude/
│   └── commands/              ← the core lifecycle slash commands
│       ├── discover.md        ← niche, ICP, competitive landscape
│       ├── position.md        ← offer definition, messaging, differentiation
│       ├── price.md           ← pricing models, packaging, objection handling
│       ├── pitch.md           ← proposals, outreach, follow-up sequences
│       ├── deliver.md         ← project/workflow/app delivery playbook
│       ├── operate.md         ← onboarding, contracts, tools stack
│       ├── grow.md            ← case studies, referrals, upsells
│       └── promote.md         ← turn any business moment into content (see below)
│
├── tracks/
│   ├── consulting/            ← discovery calls, scope docs, SOW templates
│   ├── workflows/             ← automation stack guides, handoff docs
│   └── apps/                  ← MVP scoping, go-to-market, non-tech approach
│
├── templates/                 ← ready-to-use business docs
│   ├── proposals/
│   ├── contracts/
│   ├── client-onboarding/
│   └── case-studies/
│
├── skills/                    ← deeper guidance files the commands draw from
│   ├── business-strategy.md
│   ├── client-communication.md
│   ├── pricing-models.md
│   ├── ai-tools-landscape.md
│   └── self-promotion.md      ← how to talk about your work without feeling like you're bragging
│
└── docs/
    ├── GETTING-STARTED.md     ← hand-holding walkthrough
    ├── LEARNING-PATH.md       ← Starter → Builder → Operator → Grower
    ├── WORKSHOPS.md           ← Build Hour session recaps and links
    └── CONTRIBUTING.md        ← how community members can add to it
```

---

## The Business Lifecycle

```
/discover  →  /position  →  /price  →  /pitch  →  /deliver  →  /operate  →  /grow
```

Each command works **standalone OR as a sequence**:
- Someone with a client call tomorrow just needs `/pitch`
- Someone starting from scratch runs them in order

---

## Promotion as a Thread, Not a Step

> **Patty:** We need to ensure we include promoting our business, product, etc. EVERY step of the way. That is something most of us struggle with so we really need AI help for this.

This is woven into every command — not a single step at the end. Every command generates a **"Now share it"** section with ready-to-post content:

| Command | Promotion built in |
|---|---|
| `/discover` | "Here's the niche I'm going after and why" post |
| `/position` | Craft your founder origin story for social |
| `/price` | Educate your audience on how you charge and why |
| `/pitch` | Turn a proposal win into a "what I learned" post |
| `/deliver` | Behind-the-scenes of your process / a client result |
| `/operate` | "Tools I use to run my AI business" content |
| `/grow` | Case study, testimonial request, referral ask |

Plus a `skills/self-promotion.md` covering:
- How to talk about your work without feeling like you're bragging
- Repurposing one thing into 5 pieces of content
- Building in public as a trust-building strategy (not self-promotion — service to your audience)

---

## Teaching Along the Way

> **Patty:** It's important to teach along the way — not to overwhelm, but to help our members learn and grow. What could that look like?

Learning through doing. Members don't study before they use the toolkit — they learn as a byproduct of using it.

### "The Why" — one sentence at the top of each command
Before Claude does anything, it gives one plain-English explanation. Not a lecture — just enough context so the output makes sense.
> *"An ICP (Ideal Client Profile) helps you stop marketing to everyone and start attracting the right people."*

### "What you just did" — one line at the end of every output
After Claude generates something, it closes with a brief explanation of what happened and why it matters.
> *"You just defined your niche. This is the hardest thing most AI business owners never do — and you did it in 10 minutes."*

### A `/teach-me` command
When someone wants to go deeper — "what IS a retainer?", "why do I need a contract?", "what's the difference between consulting and productized services?" — they can ask without feeling dumb. Plain business language, no jargon.

### A visible learning path (`LEARNING-PATH.md`)
```
Starter     → you know what you're offering and who it's for
Builder     → you've pitched and landed your first client
Operator    → you have systems, a process, and repeat clients
Grower      → you're getting referrals and building in public
```
Every command they complete moves them forward on that path.

### What NOT to do
No walls of text. No prerequisite reading. No "before you run this command, make sure you've read the glossary." The teaching should feel like a smart friend explaining things as you go — not a course you have to finish first.

---

## Building in Public — The WDAI Way

> **Patty:** We are thinking we may start with sharing the doc in a Build Hour Series and developing the framework and the content from there in each build hour meeting. Be truly brave and vulnerable but building in public which is sooooooo very key to WDAI mission!

This IS the product. The community doesn't just use the toolkit — they watch it get built, contribute to it, and grow with it. That's the WDAI difference.

### The Build Hour Series format (one command per session)
1. **Concept** — 5 min: Patty or Anennya share honestly where they struggled with this
2. **Demo** — 10 min: run the command live, show what comes out (messy and real)
3. **Do it** — 15 min: members run it on their own business idea
4. **Share** — 10 min: 2–3 members share what came out, what surprised them
5. **Capture** — after the session, the best member contributions get folded back into the repo

### What "building in public" looks like for this project
- Share what's working AND what's not working
- Show the messy middle, not just polished results
- Let members see the repo evolve in real time
- Celebrate member contributions publicly (credit everything)
- Document the journey: this brainstorm doc is session zero

### By Build Hour 7:
- A fully community-battle-tested toolkit
- Real member stories and case studies in the templates folder
- Authentic testimonials for when this becomes a product
- A community that owns it because they helped build it

---

## Access Model

**Recommended: dual-track**
- **GitHub** for tech-comfortable members (private repo, invite-only)
- **Companion Notion or PDF** for members who won't touch GitHub at all
- GitHub = source of truth; Notion/PDF = friendly front door

---

## Open Questions / Next Steps

- [ ] Does WDAI already have a GitHub org, or does one need to be created?
- [ ] Which Build Hour session do we use to launch this? That date drives what we build first
- [ ] Who are the first 2–3 founding members to help us test and shape `/discover` live?
- [ ] Notion vs. another tool for the non-GitHub version?
- [ ] Do Patty and Anennya each want their own `/promote` voice profile, or a shared WDAI leadership voice?

**Suggested first build:** `CLAUDE.md` + `/discover` command ready for the first Build Hour session.

---

*This doc was created live during Claude Code's Build Together Office Hours and updated across multiple sessions. It IS the building in public.*
