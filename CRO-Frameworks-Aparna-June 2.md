# CRO Frameworks — Evergreen Best Practices

**Session with Claude Code — June 2, 2026**
*Participant: Aparna*
*Purpose: Identify the evergreen, best-practice frameworks the CRO (Chief Revenue Officer) role should draw from, sourced from Harvard Business Review, established sales/pricing thought leadership, and books that have stood the test of time. Command naming follows a beginner-friendly logic.*

---

## How a CRO Operates — Explained to a Beginner Founder

**The one-line version:** The CRO turns interest into income. If the CMO gets the right people to know and trust you, the CRO is the one who actually has the conversation, makes the offer, names the price, and closes the deal — then turns that one client into the next two.

### The four things every CRO really does

Strip away the corporate language and every CRO — from a Fortune 500 to a solo consultant — does four things:

1. **Designs the offer.** Decides exactly what you sell — turning "AI consulting" into a concrete, named, fixed-price package a buyer can say yes to without anxiety.
2. **Sets the price.** Figures out what to charge based on the *value to the client*, not the hours you put in — and learns to say the number out loud without flinching.
3. **Has the sales conversation.** Reaches the right people, listens to their real problem, and structures a pitch that helps them see why solving it (with you) is worth it.
4. **Grows the revenue.** Turns each happy client into referrals, case studies, and repeat work — so you're not starting from zero every month.

### The mindset shift that defines the role

The hardest reframe for this audience: **selling is not convincing — it's diagnosing.** Most WDAI members dread sales because they picture pushy persuasion. The research-backed truth (SPIN Selling, 35,000 sales calls studied) is the opposite: in successful sales, *the buyer talks more than the seller.* Your job is to ask good questions and help the client articulate their own need. Done right, selling feels like consulting — which is exactly what this audience is good at.

The second reframe, from value-based pricing: **charge for the outcome, not your time.** A workflow that saves a client $100K/year is worth far more than "10 hours of work." Under-charging is the most common mistake new founders make — and it signals low confidence, attracts difficult clients, and starves the business.

### Why the CRO is the "uncomfortable but unavoidable" role

This is the role most WDAI members instinctively avoid — they under-charge, dodge the close, and forget to ask for the referral. But a business without revenue is a hobby. The CRO frameworks exist to make the uncomfortable moves (naming a price, asking for the sale, asking for a referral) *systematic and scripted* instead of awkward and improvised. Notably, the CRO was missing entirely from the original lifecycle design — "find clients" and "pricing" were split across `/pitch` and `/price` but nobody owned the revenue motion end-to-end. This role fixes that.

---

## Mapping to Our Repo's CRO Scope

Per the May 5 brainstorm, the CRO owns Phase 1 Items 4, 5, 13. Patty's Phase-1-Frameworks already covers strong executional ground:

| Phase 1 Item | Patty's Existing Framework | Gap to Fill |
|---|---|---|
| Item 4 — Find first clients | Warm-to-Cold Progression + Referral Map + Hormozi First 5 | Solid; needs a beachhead-outreach lens |
| Item 5 — Pricing | 3-Tier Pricing Ladder + Value-Based Formula + Pricing Sanity Check | Needs a *consulting-services* pricing philosophy (Stark, Enns) + offer design framework |
| Item 13 — Grow beyond first client | Growth Flywheel + Case Study Template + Referral Ask + Upsell Ladder | Solid; needs a measurement framework (NPS) + modern funnel lens |
| **(missing from Phase 1)** | — | Sales discovery + structured sales pitch — neither exists yet in the repo |

The frameworks below **layer on top of Patty's work** and **fill two real gaps**: sales discovery (the conversation between outreach and proposal) and the sales pitch itself (how to actually pitch when you're in the room).

---

## The Recommended Evergreen Frameworks

### 1. Offer Design — Hormozi's Value Equation + Productized Service Model ★ (What you're selling)

**Source:** Alex Hormozi, *$100M Offers* (2021) for the Value Equation; Brian Casel & Jane Portman's productized service literature for the structural pattern.

**What it is:** Two ideas working together:

- **The Value Equation:** Perceived value = (Dream Outcome × Perceived Likelihood of Achievement) ÷ (Time Delay × Effort & Sacrifice). Tune the numerator up, the denominator down, and the offer becomes a no-brainer.
- **Productized Service Model:** Fixed scope + fixed price + repeatable delivery. Replaces "I do AI consulting" (vague, hourly, scary) with "AI Operations Audit — $2,500, 5 business days, delivered as a 12-page report" (concrete, fixed, easy to say yes to).

**Why it fits:** Most WDAI members try to sell "AI services" and freeze when asked "what exactly?" The Value Equation forces clarity on what the client actually gets, and productization removes the open-ended scope that creates pricing anxiety. Patty's 3-Tier Ladder is the *structure* — the Value Equation is the *test* each tier has to pass.

**How it powers commands:** This framework powers BOTH `/cro-draft-offer` (a v0 hypothesis to start conversations) and `/cro-final-offer` (the refined offer after discovery). Same framework, two passes — see the sequencing section below.

---

### 2. Value-Based Pricing — Stark + Enns ★ (How much to charge)

**Source:** Jonathan Stark, *Hourly Billing Is Nuts* (2017) for the philosophical case; Blair Enns, *Pricing Creativity* (2018) and *The Win Without Pitching Manifesto* (2010) for the practical method.

**What it is:** Stop charging for your time; charge for the *value created*. Enns operationalizes this with three rules: **(1) Always offer three options** (not one); **(2) Let the client see the price ladder** (anchors expectations); **(3) Quote value, not effort** (a $10K project that saves the client $100K is a 10x deal, not "expensive").

**Why it fits:** This pairs perfectly with Patty's Value-Based Pricing formula (charge 10-20% of the value you create). Stark gives the *why* — value-based pricing is a philosophical break from time-for-money. Enns gives the *how* — always three options, always value-anchored. The "Pricing Sanity Check" Patty already wrote ("if you want to apologize after saying it, it's probably the right price") is pure Enns.

**How it powers a command:** `/cro-pricing` calculates the value the client receives, sets pricing at 10-20% of that value, expresses it in three options (Enns), and produces a Pricing Sheet with the explicit *why* for each tier. Inherits the final offer from `/cro-final-offer`.

---

### 3. The Warm-to-Cold Outreach Progression + Beachhead Outreach

**Source:** Patty's Phase-1-Frameworks-Patty.md (Item 6 — already documented); layered with the *Beachhead* concept from Bill Aulet's *Disciplined Entrepreneurship* (MIT, 2013) and Hormozi's *First 5 Clients* framework (already in Phase-1-Consolidated).

**What it is:** Don't broadcast — concentrate. Pick the smallest tight segment where you can reach 50+ right-fit people through *warm* introductions, dominate that segment, then expand. Patty's existing Warm-to-Cold Progression (network → LinkedIn → community → cold email) is the executional path; the Beachhead insight is the discipline (resist the urge to "spray and pray").

**Why it fits:** The Phase 1 research is explicit: warm referrals convert dramatically higher than any other channel for early-stage consultants, and your first client almost always comes from your existing network — not cold outreach. Beachhead-outreach makes this strategic instead of accidental.

**How it powers a command:** `/cro-outreach` produces a 50-person warm contact map (Patty's Referral Map), tagged by ICP fit and "comfort level," with a sequenced 90-day outreach plan. Output: a tracked outreach pipeline with 3 conversations scheduled by week 2.

---

### 4. SPIN Selling — Sales Discovery ★ (How to have the conversation)

**Source:** Neil Rackham, *SPIN Selling* (1988). Based on a 12-year, 35,000-call research study at Huthwaite — the most rigorously researched B2B sales methodology ever published. Still the bedrock of every modern consulting sales course.

**What it is:** Four question types, asked in order, that lead a buyer to articulate their own need:

- **S**ituation — Understand the current state
- **P**roblem — Surface specific dissatisfactions
- **I**mplication — Make the cost of the problem real and felt
- **N**eed-payoff — Let the buyer articulate the value of solving it

The killer insight: in successful sales calls, **the buyer talks more than the seller**, and the seller's questions move from Situation → Problem → Implication → Need-payoff. Bad sellers stay stuck in Situation questions. Great sellers escalate to Implication.

**Why it fits:** This is the missing piece in Patty's framework. Phase 1 has prospecting (warm outreach) and pricing (the ladder) but nothing about the conversation in between. SPIN turns a sales call from "let me pitch you my services" into "let me help you articulate what you actually need" — which is also closer to how WDAI members naturally want to operate. **This is also where the founder learns what to put in the final offer and how to price it.**

**How it powers a command:** `/cro-discovery` produces a SPIN-structured discovery script tailored to the founder's niche — 15-20 questions across the 4 categories, with branching follow-ups. Output: a discovery doc + a "buyer pain map" capturing what the prospect said, used as input to `/cro-final-offer`, `/cro-pricing`, and `/cro-pitch`.

---

### 5. Dunford's Sales Pitch + Cialdini's Remaining Three ★ (How to pitch and close)

**Source:** April Dunford, *Sales Pitch* (2023) — the structural backbone. Robert Cialdini, *Influence* — Reciprocity, Commitment/Consistency, Scarcity (the three principles we deferred from CMO because they're closing levers, not credibility levers).

**What it is:** Dunford's *Sales Pitch* is the only modern, founder-era framework for actually delivering a B2B sales pitch. Five components in order:

1. **Insight** — open with a market insight the prospect hadn't considered (Challenger-style)
2. **Alternatives & Trade-offs** — name competitive alternatives explicitly and their flaws
3. **Perfect-World** — describe what an ideal solution would look like (your differentiators)
4. **Introducing Us** — only NOW introduce your offer, framed against the perfect-world criteria
5. **Proof** — credibility evidence (Cialdini's Authority + Social Proof from `/cmo-credibility`)

Then layer Cialdini's three closing principles:
- **Reciprocity** — give something concrete before asking (a free mini-audit, a custom insight)
- **Commitment/Consistency** — small public yes leads to larger yes (e.g., "would you agree the biggest risk is X?")
- **Scarcity** — limited capacity is real for solo consultants ("I take on 3 clients per quarter"), not manufactured

**Why it fits:** This replaces the generic "pitch deck" mental model with a structured conversation that earns the right to be considered. Pairs perfectly with Patty's "Show, Don't Tell Demo" — Dunford's framework is the conversational scaffolding around the demo.

**How it powers a command:** `/cro-pitch` produces a 5-section Pitch Sheet tailored to a specific prospect (uses the discovery doc as input) + a closing playbook applying Cialdini's three principles. Output: ready-to-deliver pitch + objection-handling responses.

---

### 6. Bowtie Funnel + NPS — Growth Beyond the First Client

**Source:** *Winning by Design*'s Bowtie Funnel for the conceptual model; Fred Reichheld's NPS (Net Promoter Score) — originally introduced in HBR's "The One Number You Need to Grow" (Dec 2003) — for the referral measurement system. Plus Patty's existing Growth Flywheel + Case Study Template + Referral Ask + Upsell Ladder.

**What it is:** Two ideas:

- **Bowtie Funnel** — the modern replacement for the traditional sales funnel. Adds *Onboard → Adopt → Expand → Advocate* on the right side of the bowtie. The insight: real revenue comes from the right side, not the left. For a consultant, each existing client should generate ~2 referrals and ~1 expansion deal.
- **NPS / Reichheld** — one question ("How likely are you to recommend us to a colleague, 0-10?") that predicts referral behavior. 9s and 10s are *promoters* and should be asked for the referral *right then*.

**Why it fits:** Patty's Growth Flywheel describes the steps; Bowtie + NPS make the system *measurable*. The Referral Ask script ("at peak satisfaction") becomes: ask the NPS question, and when they answer 9 or 10, you're at peak satisfaction by definition.

**How it powers a command:** `/cro-grow` produces a Growth Loop doc per client — when to ask the NPS question, when to plant the upsell, when to write the case study, when to ask for the referral. Output: a per-client growth track that turns each completed engagement into 2-3 next ones.

---

## What's Intentionally Left Out (And Why)

| Framework | Why we're skipping it |
|---|---|
| **The Challenger Sale (Dixon & Adamson)** | Great research, but designed for *complex enterprise sales teams*. Solo consultants don't need the Teach/Tailor/Take Control profile system — Dunford's *Sales Pitch* delivers the Challenger spirit in a founder-sized package. |
| **MEDDIC / MEDDPICC** | Enterprise B2B qualification framework — overkill for sub-$50K consulting deals. Add later if a member moves up-market. |
| **BANT (Budget/Authority/Need/Timeline)** | Mostly obsolete — built for outbound SDR motions, not founder-led consulting sales. SPIN does the same job better. |
| **Sandler Sales Method** | Strong methodology, but training-heavy and built for repeatable seller motions. SPIN + Dunford is enough for solo founders. |
| **Hermann Simon, Confessions of the Pricing Man** | Excellent book, but focused on corporate pricing strategy. Stark + Enns are the solo-consultant equivalent. |
| **Customer Success / Lincoln Murphy** | Important once you have 10+ clients on retainer. Add as an advanced module when the WDAI member is past first-client stage. |

---

## The 7 CRO Sub-Commands — Beginner Question Naming

| Command | Beginner's Question | Framework |
|---|---|---|
| **`/cro-draft-offer`** | "What might I sell? (rough draft)" | Hormozi Value Equation + Productized Service (v0 hypothesis) |
| **`/cro-final-offer`** | "What am I actually selling? (after talking to people)" | Hormozi Value Equation + Productized Service (refined) |
| **`/cro-pricing`** | "How much should I charge?" | Stark Value-Based Pricing + Enns Three Options + Patty's 3-Tier Ladder |
| **`/cro-outreach`** | "Where do I find people to talk to?" | Patty's Warm-to-Cold + Beachhead Outreach + Hormozi First 5 |
| **`/cro-discovery`** | "How do I have the sales conversation?" | SPIN Selling (Situation → Problem → Implication → Need-payoff) |
| **`/cro-pitch`** | "How do I pitch and close the deal?" | Dunford's Sales Pitch + Cialdini's Reciprocity/Commitment/Scarcity |
| **`/cro-grow`** | "How do I turn one client into more?" | Bowtie Funnel + NPS + Patty's Growth Flywheel |

---

## How to Actually Run Them — The Step-by-Step Sequence

The framework list above is in *logical* order (how the pieces fit together). But that is **not** the order a beginner should run them. There is a chicken-and-egg trap: you cannot finalize an offer or a price in a vacuum. A founder who perfects their offer and pricing before talking to a single human will build something nobody wants — the exact mistake `/ceo-validate` exists to prevent.

So the right sequence is a **draft → talk → refine loop**, not a straight line:

```
STEP 1   /cro-draft-offer  →  DRAFT a v0 offer (a hypothesis, not final)
STEP 2   /cro-outreach     →  Build the warm list, start conversations
STEP 3   /cro-discovery    →  Listen first (SPIN) — this is where you LEARN
              ↓
         ┌──── informed by what you heard ────┐
STEP 4   /cro-final-offer                      │  Sharpen the offer
STEP 5   /cro-pricing                          │  NOW price it
         └───────────────────────────────────-┘
              ↓
STEP 6   /cro-pitch        →  Pitch and close
STEP 7   /cro-grow         →  Turn each win into the next two
```

### Why this order

| Move | Why it's here |
|---|---|
| **Draft offer first** | You need *something* to react to. A rough "I think I help X do Y" is enough to start a conversation. Don't polish it yet. |
| **Outreach before pricing** | Get in front of people fast. Patty's research is explicit: warm conversations are the fastest path to signal. Waiting until pricing is "ready" is procrastination disguised as prep. |
| **Discovery before finalizing** | SPIN is where you learn what they actually need and what the pain is worth. This *informs* both the final offer and the price. |
| **Final offer + pricing late** | Enns/Stark value-based pricing requires knowing the value to the client — which you only learn in discovery. You literally cannot price well until Step 3 is done. |
| **Pitch, then grow** | These two are genuinely sequential and come last. |

### The one rule to give beginners

> **"Draft your offer in pencil. Talk to 5 people. Then write your offer and price in pen."**

This captures the loop without the jargon. It also connects cleanly to the CEO workflow — `/cro-outreach` + `/cro-discovery` are essentially where the founder runs Patty's 10-Conversation validation test, so the CRO sequence and `/ceo-validate` overlap by design.

**The sequence reads as a sentence:** *Sketch the offer → go talk to people → listen hard → finalize the offer → price it → pitch and close → grow from each win.*

---

## How These Frameworks Connect

```
   DRAFT OFFER (Hormozi — rough hypothesis)
        ↓
   OUTREACH (Warm-to-Cold + Beachhead)
        ↓
   DISCOVERY (SPIN Selling) ── the learning engine
        ↓
   FINAL OFFER (Hormozi — refined with what you heard)
        ↓
   PRICING (Stark + Enns three options)
        ↓
   PITCH (Dunford Sales Pitch + Cialdini close)
        ↓
   GROW (Bowtie Funnel + NPS + Patty's Growth Flywheel)
```

The CRO funnel is *not* "find leads → close them." It's: sketch an offer worth discussing, reach the right people warmly, listen until you understand the value, finalize and price against that value, structure the pitch, then turn each yes into the next yes.

---

## Connection to Other C-Suite Workflows

- **CEO → CRO:** Niche, ICP, and JTBD set the segment the CRO is selling to. The "winning aspiration" from `/ceo-strategy` defines what revenue success looks like. `/cro-outreach` + `/cro-discovery` overlap with `/ceo-validate`'s 10-conversation test.
- **CMO → CRO:** The BrandScript from `/cmo-messaging` becomes the source for pitch language. The Credibility Stack from `/cmo-credibility` feeds Dunford's "Proof" component. The audience from `/cmo-audience` is the warm outreach list for `/cro-outreach`.
- **CRO → COO:** Once a deal closes, COO's onboarding (contracts, SOW, kickoff) takes over. The pricing decisions in `/cro-pricing` drive payment terms in COO's contract templates.
- **CRO → CPO:** Pricing and packaging constraints set the scope the CPO has to fit MVP within.
- **CRO ↔ CMO:** Lost deals and won deals feed back to CMO — recurring "we went with X" triggers `/cmo-positioning` refresh.

---

## Connections — The `/launch` Convergence Command

When `/launch` runs, it pulls these CRO artifacts as inputs:

| CRO command output | What `/launch` uses it for |
|---|---|
| `/cro-final-offer` → Offer Sheet | The "what we're selling" anchor for the launch announcement |
| `/cro-pricing` → Pricing Sheet | The price point that goes on the landing page and pitch |
| `/cro-outreach` → 90-day outreach plan | The launch-week pipeline — who gets the personal outreach |
| `/cro-discovery` → discovery script | Sales-ready conversation flow for inbound launch leads |
| `/cro-pitch` → Pitch Sheet | Pitch deck / landing page sales copy |
| `/cro-grow` → Growth Loop | The post-launch flywheel (case studies + referrals from first launch clients) |

CRO is the most *operational* of the launch inputs — without the final offer and pricing locked in, `/launch` cannot proceed.

---

## Triggers and Trigger Re-Entry

### When the FULL CRO sequence runs

| Trigger | What just happened | Why the full sequence re-fires |
|---|---|---|
| **New startup** | Founder starting from zero | Need draft offer → outreach → discovery → final offer → pricing → pitch → growth from scratch |
| **Major pivot** | `/ceo-pivot` declared | Old offer + pricing dead; sales motion must reset (back to draft offer) |
| **New market entry** | Expanding to a second niche | Each market needs its own offer/pricing/outreach motion |

### When a SUBSET re-fires

| Trigger | What just happened | Commands that re-fire | Why |
|---|---|---|---|
| **Hitting close-rate ceiling** | Pitching ≥10 deals, closing <20% | `/cro-discovery` + `/cro-pitch` | Either discovery is too shallow or pitch is misfiring |
| **Heard "you're too expensive" 3+ times** | Price objections clustering | `/cro-pricing` + `/cro-final-offer` | Either price is misaligned to value, or offer doesn't justify the price |
| **First case study lands** | Quotable client result | `/cro-pitch` (add proof) + `/cro-grow` (referral ask) | New proof to slot into Dunford's Proof component + activate referral |
| **Dry pipeline (no conversations in 30 days)** | Outreach isn't producing | `/cro-outreach` + `/cmo-audience` | Either outreach mechanics are broken or audience pool is too small |
| **Lost a deal to a specific competitor** | "We went with X" 2+ times | `/cro-final-offer` + `/cro-pitch` + `/cmo-positioning` | Competitive frame has shifted — repositioning + offer audit |
| **Discovery keeps surfacing a different pain** | Prospects consistently want something you don't offer | `/cro-final-offer` (re-shape) | The market is telling you to change the offer |
| **Client doesn't refer despite high satisfaction** | NPS 9-10 but no introductions | `/cro-grow` (audit the referral ask timing) | Referral mechanic is broken even though sentiment is positive |
| **Quarterly review** | End of OKR cycle | `/cro-grow` (review conversion + expansion rates) | Periodic health check |
| **Hiring a sales hand / VA** | About to delegate outreach | `/cro-outreach` + `/cro-discovery` (formalize as a playbook) | The output is the doc the new person needs |

### Convergence triggers

| Trigger | Commands across roles |
|---|---|
| **Go-to-market launch** | Full CRO sequence locked → handoff to `/launch` |
| **First client signed** | `/cro-grow` (start the loop) + COO onboarding + CMO `/cmo-content` (announce) |
| **Pivot decision** | `/ceo-pivot` → `/cro-draft-offer` (reset) → re-run the loop |
| **First case study** | `/cro-grow` + `/cmo-credibility` + `/cmo-content` (1-to-5 from the win) |

---

## Open Questions / Next Steps

- [ ] Validate with Patty and Anennya
- [ ] Should the WDAI version include a "consulting vs. workflows vs. apps" pricing branch in `/cro-pricing`, given the three tracks have very different pricing realities?
- [ ] Confirm the sales discovery (CRO) vs. delivery discovery (COO) boundary when we get to COO — both involve a "discovery" conversation but with different purposes (sell vs. scope)
- [ ] Move on to **COO** next — candidate shortlist: Eliyahu Goldratt (*The Goal* — Theory of Constraints), W. Edwards Deming (PDCA cycle), Michael Gerber (*The E-Myth Revisited*), Gino Wickman (*Traction* — EOS), RACI matrix, Patty's Client Project Lifecycle + SOW Template + Invoice Template (already in repo).

---

## Sources

- Hormozi, A. *$100M Offers: How to Make Offers So Good People Feel Stupid Saying No*. Acquisition.com, 2021.
- Stark, J. *Hourly Billing Is Nuts*. 2017. / Enns, B. *Pricing Creativity: A Guide to Profit Beyond the Billable Hour*. The Win Without Pitching, 2018.
- Enns, B. *The Win Without Pitching Manifesto*. 2010.
- Aulet, B. *Disciplined Entrepreneurship*. Wiley, 2013.
- Rackham, N. *SPIN Selling*. McGraw-Hill, 1988.
- Dunford, A. *Sales Pitch: How to Craft a Story to Stand Out and Win*. Ambient Press, 2023.
- Cialdini, R. *Influence: The Psychology of Persuasion* (Revised Edition). Harper Business, 2021.
- Reichheld, F. ["The One Number You Need to Grow"](https://hbr.org/2003/12/the-one-number-you-need-to-grow). Harvard Business Review, December 2003.
- Winning by Design. *The Bowtie Funnel / Revenue Architecture* methodology.
- O'Brien Novak, P. *Phase-1-Frameworks-Patty.md* (WDAI repo, April 2026).
