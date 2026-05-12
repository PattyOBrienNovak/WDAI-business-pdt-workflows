# CEO Frameworks — Evergreen Best Practices

**Session with Claude Code — May 12, 2026**
*Participant: Aparna*
*Purpose: Identify the evergreen, best-practice frameworks the CEO role should draw from, sourced from Harvard Business Review, established business thought leadership, and books that have stood the test of time.*

---

## What the CEO Owns

The CEO sets the founding bet — who you serve, where you'll play, how you'll win, and what success looks like. For an early-stage AI business, this is the highest-leverage role. Get it wrong and every other workflow (CMO, CRO, COO, CPO, CTO, CDO) runs in the wrong direction.

---

## The Recommended Evergreen Frameworks

### 1. Playing to Win — The Strategic Choice Cascade ★ (Backbone framework)

**Source:** A.G. Lafley & Roger Martin, *Playing to Win* (Harvard Business Review Press, 2013). Roger Martin is consistently ranked the #1 management thinker in the world. This is THE strategy framework recommended by HBR.

**What it is:** Five questions, asked in order, that define a strategy:

1. **What is our winning aspiration?** (What does winning look like for us?)
2. **Where will we play?** (Which markets, customers, channels, geographies?)
3. **How will we win?** (What's our competitive advantage?)
4. **What capabilities must we have?** (What must we be uniquely good at?)
5. **What management systems do we need?** (How do we measure, learn, and adjust?)

**Why it fits:** The most rigorous yet accessible strategy framework that exists. It forces founders to make *choices* — Martin's core point is that "strategy is choice." Most WDAI members default to "I help businesses use AI" — Playing to Win is the antidote.

**How it powers a command:** `/ceo-strategy` walks the founder through all 5 questions in order. Output is a one-page "Strategic Choice Cascade" doc that becomes the canonical reference for every other C-suite workflow.

---

### 2. The Hedgehog Concept ★ (Focus framework)

**Source:** Jim Collins, *Good to Great* (HarperBusiness, 2001). One of the most-cited business books of the last 25 years.

**What it is:** The intersection of three circles:
- What you can be **the best in the world at**
- What you are **deeply passionate about**
- What drives your **economic engine** (where the money is)

You don't pick what you want to do — you find what sits at the intersection. Collins found great companies took ~4 years to fully crystallize this.

**Why it fits:** Perfect for the niche-picking moment. WDAI members come from rich, varied backgrounds — finance, HR, healthcare, marketing. The Hedgehog forces them to identify where their existing expertise + AI capability + paying market actually overlap. It's also a great teaching moment because it explicitly gives permission to say no to opportunities outside the intersection.

**How it powers a command:** `/ceo-hedgehog` produces the three-circle output and forces them to name what they're saying NO to.

---

### 3. Jobs to Be Done (JTBD) ★ (Customer truth framework)

**Source:** Clayton Christensen (Harvard Business School), *Competing Against Luck* (2016). The HBR article "Know Your Customers' Jobs to Be Done" is one of HBR's most-read pieces ever.

**What it is:** "People don't buy products; they hire them to do a job." You're not selling AI — you're being hired to make a specific situation in someone's life better. The job is functional, emotional, and social.

**Why it fits:** This is the antidote to "I build AI workflows." It forces you to articulate what your client is firing (their current solution) and hiring you to do instead. It's also the bridge between CEO work and CMO/CPO work — both downstream roles inherit the JTBD definition.

**How it powers a command:** `/ceo-job` produces a "Job Statement" in Christensen's format: *"When [situation], I want to [motivation], so I can [expected outcome]."*

---

### 4. The Theory of the Business (The 3 Assumptions Test)

**Source:** Peter Drucker, "The Theory of the Business" (HBR, Sept-Oct 1994). One of HBR's most influential articles ever — written 32 years ago and still essential reading.

**What it is:** Every business runs on three assumptions:
1. **Assumptions about the environment** — society, markets, customers, technology
2. **Assumptions about the mission** — what we're here to do
3. **Assumptions about core competencies** — what we must be excellent at

The killer insight: most businesses fail not because they execute poorly, but because their *assumptions* become invalid and nobody notices. Drucker says the assumptions must (a) fit reality, (b) fit each other, (c) be known throughout the org, (d) be tested constantly.

**Why it fits:** AI is changing so fast that yesterday's assumptions become wrong in months. Building this into the CEO workflow makes "test your assumptions" a habit, not a one-time exercise. This is also the foundation for the trigger model from Anennya's May 5 brainstorm — the trigger is *"an assumption broke."*

**How it powers a command:** `/ceo-assumptions` writes down the three assumptions explicitly. Every quarter, `/ceo-review` re-tests them.

---

### 5. The Lean Startup Loop — Build-Measure-Learn

**Source:** Eric Ries, *The Lean Startup* (2011), built on Steve Blank's Customer Development. The single most influential founder framework of the last 15 years.

**What it is:** Treat your business as a series of testable hypotheses. Form a hypothesis → build the smallest test → measure real behavior → learn → either persevere or pivot. Each loop should be days or weeks, not quarters.

**Why it fits:** Patty's Phase-1 already includes validation (3-Filter + 10-conversation test) — this is the parent framework that contextualizes it. It also gives a name to "pivot" as a strategic move, not a failure.

**How it powers a command:** `/ceo-validate` (Phase 1 already designed this) plus `/ceo-pivot` for the moment when learning says "the original bet was wrong."

---

### 6. OKRs — Objectives & Key Results

**Source:** Originated by Andy Grove (Intel), popularized by John Doerr in *Measure What Matters* (2018). Used by Google, Stripe, basically every well-run tech company.

**What it is:** One **Objective** (qualitative, ambitious, inspiring) paired with 3-5 **Key Results** (quantitative, measurable, time-bound). Set quarterly. Score them at the end.

**Why it fits:** Gives the solo founder structure for what "winning" looks like in 90 days. Without OKRs, founders drift between tasks. With them, they know what to say no to.

**How it powers a command:** `/ceo-okrs` sets quarterly objectives. `/ceo-review` scores them and resets.

---

## What's Intentionally Left Out (And Why)

| Framework | Why we're skipping it |
|---|---|
| **Porter's Five Forces** | Brilliant framework, but designed for established companies analyzing industry structure. Too abstract for a solo founder still finding their niche. |
| **Blue Ocean Strategy** | Useful concept, but the "value innovation canvas" is overkill at this stage and assumes you already know your category. |
| **Wardley Mapping** | Powerful for tech strategy, but the learning curve is steep. Better as an advanced/optional add-on later. |
| **BCG Growth-Share Matrix** | For multi-product portfolios. A solo AI consultant doesn't need it. |
| **SWOT** | So overused it's become noise. Most founders fill it out and learn nothing. Skip. |

---

## How These Frameworks Connect

```
  PLAYING TO WIN (the structural choices)
        ↓
  HEDGEHOG (focus discipline — what you can win at)
        ↓
  JTBD (the customer truth that grounds the bet)
        ↓
  THEORY OF THE BUSINESS (the assumptions underneath it all)
        ↓
  LEAN STARTUP LOOP (how you test and refine)
        ↓
  OKRs (how you operationalize quarter-by-quarter)
```

Each framework hands its output to the next. Playing to Win names the choices; Hedgehog disciplines them with a focus test; JTBD grounds them in real customer behavior; Theory of the Business surfaces the assumptions underneath the choices so they can be tested; Lean Startup tests them; OKRs operationalize them quarter by quarter.

---

## The 6 CEO Sub-Commands

Based on the frameworks above, the CEO workflow has 6 sub-commands:

| Command | Framework | What it does |
|---|---|---|
| **`/ceo-strategy`** | Playing to Win | Walks the founder through the 5-question Strategic Choice Cascade. Output: one-page strategy doc — winning aspiration, where to play, how to win, capabilities, management systems. The canonical reference for every other C-suite workflow. |
| **`/ceo-hedgehog`** | Hedgehog Concept | Forces the three-circle test: what you can be the best at × what you're passionate about × what drives the economic engine. Output: the founder's Hedgehog statement plus an explicit "saying NO to" list. |
| **`/ceo-job`** | Jobs to Be Done | Names the job the client is hiring you to do. Output: a Christensen-format Job Statement — "When [situation], I want to [motivation], so I can [expected outcome]." Inherited by CMO and CPO workflows. |
| **`/ceo-assumptions`** | Theory of the Business | Surfaces the three sets of assumptions (environment, mission, core competencies). Output: an explicit Assumptions Doc. Re-tested in every `/ceo-review`. |
| **`/ceo-validate`** / **`/ceo-pivot`** | Lean Startup Loop | `/ceo-validate` runs Patty's 3-Filter + 10-Conversation test (Phase 1). `/ceo-pivot` is the explicit reset moment — triggered when assumptions break or validation comes back negative. Output: pivot decision doc. |
| **`/ceo-okrs`** | OKRs | Sets one quarterly Objective + 3-5 Key Results. Output: quarterly OKR doc. Reviewed and scored every 90 days in `/ceo-review`. |

---

## Connection to Other C-Suite Workflows

The CEO outputs are inputs to every other role:

- **CEO → CMO:** Niche, ICP, JTBD, positioning anchor feed `/cmo-position` and `/cmo-message`.
- **CEO → CRO:** Winning aspiration and ICP drive pricing and sales motion.
- **CEO → COO:** Capabilities required (Playing to Win question 4) inform what operations need to support.
- **CEO → CPO:** Job to Be Done is the foundation of `/cpo-define`.
- **CEO → CTO/CDO:** Strategic choices set the constraints (build vs. buy, brand premium vs. utility, etc.).

This is why the CEO workflow runs first in any "new company" trigger from Anennya's iterative model.

---

## Open Questions / Next Steps

- [ ] Validate this framework selection with Patty and Anennya
- [ ] Draft the 6 CEO sub-command files (`.md` format for `.claude/commands/`)
- [ ] Decide: do these frameworks live as named blocks inside each command, or as a separate reference doc both members and Claude can reference?
- [ ] Move on to **CMO** frameworks next — candidate shortlist: April Dunford (Obviously Awesome), Donald Miller (StoryBrand), Byron Sharp (How Brands Grow), Seth Godin (Purple Cow / Permission Marketing), Joe Pulizzi (Content Marketing pillars).

---

## Sources

- Lafley, A.G. & Martin, R.L. *Playing to Win: How Strategy Really Works*. Harvard Business Review Press, 2013. https://store.hbr.org/product/playing-to-win-expanded-with-bonus-hbr-articles-how-strategy-really-works/10852
- Martin, R.L. ["The Ultimate Guide to Strategy"](https://www.lennysnewsletter.com/p/the-ultimate-guide-to-strategy-roger-martin), Lenny's Newsletter.
- Collins, J. *Good to Great*. HarperBusiness, 2001. https://www.jimcollins.com/concepts/the-hedgehog-concept.html
- Christensen, C.M., Hall, T., Dillon, K., & Duncan, D.S. ["Know Your Customers' Jobs to Be Done"](https://hbr.org/2016/09/know-your-customers-jobs-to-be-done). Harvard Business Review, September 2016.
- Drucker, P.F. ["The Theory of the Business"](https://hbr.org/1994/09/the-theory-of-the-business). Harvard Business Review, September-October 1994.
- Ries, E. *The Lean Startup*. Crown Business, 2011.
- Doerr, J. *Measure What Matters*. Portfolio, 2018.
