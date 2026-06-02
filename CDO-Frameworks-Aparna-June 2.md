# CDO (Design) Frameworks — Evergreen Best Practices

**Session with Claude Code — June 2, 2026**
*Participant: Aparna*
*Purpose: Identify the evergreen, best-practice frameworks the CDO (Chief Design Officer) role should draw from, sourced from established design thought leadership. Reconciles with Anennya's May 5 design-track command design. Command naming follows a beginner-friendly logic.*

> **Scope note:** The CDO role splits into two tracks with different reach:
> - **Brand track** (`/design-brand`) — useful for **all three tracks**, including consulting. Every business needs a visual identity.
> - **UX track** (`/design-user`, `/design-flows`, `/design-system`, `/design-test`) — **apps/workflows only.** You need a product to design a user experience for.
>
> Command prefix is `/design-` (not `/cdo-`) — "design" is far more discoverable than "CDO," the least-known C-suite title.

---

## How a CDO Operates — Explained to a Beginner Founder

**The one-line version:** The CDO decides *how the product looks, how it feels to use, and whether people can actually figure it out* — plus the visual identity the whole business presents to the world.

### The most important reframe for a beginner

Most beginners think design means *making it pretty.* It doesn't. The defining principle (Steve Jobs said it best):

> **"Design is not just what it looks like. Design is how it works."**

A beautiful product nobody can navigate is a failure. A plain product that's effortless to use is a success. The CDO's real job is **clarity and trust**, not decoration.

### A reality specific to a Claude Code toolkit

Claude produces **text, not pixels.** So the CDO role here doesn't draw screens — it produces:
- **Design briefs and specs** (the thinking: who, what flow, what structure — the hard part)
- **Prompts formatted for visual tools** (Figma, v0, Canva, Midjourney) that the founder runs to generate the actual visuals

This is liberating for a non-designer founder: the CDO commands do the *structural design thinking* and hand off the *pixel-making* to AI design tools.

### The four things every CDO really does

1. **Defines the look and feel.** Turns the brand strategy into an actual visual identity.
2. **Understands the user's world.** Who are they, what's their day like, where does the product fit?
3. **Maps how users move through it.** What screens, in what order, where do they get confused?
4. **Makes it usable and consistent.** Reusable patterns + testing with real people.

### The mindset shift that defines the role

Beyond "design is how it works," the second reframe is **the user is not you.** Founders design for themselves by default — they know where everything is because they built it. The CDO's discipline is to design for someone who has never seen the product, is busy, and will leave the moment they're confused. This is why *testing with real users* (not asking friends if they like it) is a core CDO command, not an afterthought.

### The AI-specific layer (the differentiator)

Just as CPO has "AI behavior cards" and CTO has "evals," the CDO owns **AI interaction patterns** — designing the probabilistic, sometimes-wrong experience:
- Loading states while the AI thinks
- Confidence indicators (how sure is the AI?)
- "Regenerate" affordances
- "AI-generated" labels (transparency)
- What the user *sees* when the AI is uncertain or wrong

This is how design builds **trust** in an AI product — the single biggest design challenge unique to this space. It's the visual/experiential counterpart to the CPO's AI behavior cards and the CTO's fallback behavior.

### Why the CDO is the "trust and clarity" role

For an AI product, design is how you signal trustworthiness. When the AI is unsure, a good design says so gracefully; a bad one either hides it (eroding trust when the user catches an error) or crashes (destroying it). A technically excellent AI product with poor design *feels* untrustworthy — and feelings drive adoption. The CDO makes a probabilistic product feel safe to rely on.

---

## The CMO vs. CDO Boundary (resolved)

This is the boundary flagged when we built the CMO doc:

| | `/cmo-brandidentity` (CMO) | `/design-brand` (CDO) |
|---|---|---|
| **Owns** | Brand *strategy* | Brand *execution* |
| **Produces** | Name, tagline, voice, color *direction*, signature phrase | Full visual system — actual palette, typography, logo direction, components |
| **Relationship** | The brief | Builds from the brief |

CMO decides *what the brand stands for and sounds like*; CDO turns that into *what it actually looks like.* `/design-brand` takes the `/cmo-brandidentity` brief as its direct input. This mirrors how real companies work: CMO owns brand strategy, design owns brand execution.

---

## Reconciling With Anennya's May 5 Design

Anennya designed 5 design-track commands in the May 5 brainstorm, organized as a Brand track + a UX track that run in parallel then converge. This doc keeps all 5 names and adds the evergreen frameworks underneath each.

| Anennya's command (May 5) | Track | Kept as |
|---|---|---|
| `/design-brand` | Brand | `/design-brand` |
| `/design-user` | UX | `/design-user` |
| `/design-flows` | UX | `/design-flows` |
| `/design-system` | UX | `/design-system` |
| `/design-test` | UX | `/design-test` |

Her AI interaction patterns concept is preserved and lives across `/design-flows` and `/design-system`.

---

## The Recommended Evergreen Frameworks

### 1. Double Diamond — The Overall Shape (How design work flows)

**Source:** British Design Council, 2005. The most widely taught model of the design process.

**What it is:** Two diamonds = two diverge-converge cycles. **Diamond 1 (the right problem):** Discover (explore widely) → Define (narrow to the real problem). **Diamond 2 (the right solution):** Develop (explore many solutions) → Deliver (narrow to the one that works). The core lesson: *don't jump to solutions before you understand the problem.*

**Why it fits:** Gives beginners the mental model for *why* the design commands are ordered the way they are — you research before you design, and you explore before you commit. It's the design counterpart to "draft your offer in pencil" from the CRO role.

**How it powers the role:** The organizing logic across all five commands — `/design-user` is Discover/Define; `/design-flows` + `/design-system` are Develop/Deliver; `/design-test` validates.

---

### 2. Design Thinking (IDEO / Stanford d.school) ★ (Human-centered method)

**Source:** Tim Brown / IDEO; Stanford d.school. Five stages: Empathize → Define → Ideate → Prototype → Test.

**What it is:** A human-centered approach that starts with deep empathy for the user, defines their real need, generates many ideas, prototypes cheaply, and tests with real people. The heart of it: **fall in love with the problem, not your solution.**

**Why it fits:** It's the most accessible design framework for non-designers and reinforces the whole toolkit's bias toward talking to real humans. The "Empathize" stage is exactly `/design-user`; "Test" is exactly `/design-test`.

**How it powers a command:** Backbone of `/design-user` (empathize + define) and the spirit of `/design-test` (prototype + test).

---

### 3. Empathy Mapping + Jobs to Be Done for UX ★ (Understanding the user)

**Source:** Empathy mapping (Dave Gray / XPLANE); JTBD applied to UX (Christensen, shared with CEO/CPO).

**What it is:** An empathy map captures what the user *says, thinks, does, and feels.* JTBD-for-UX asks what job they're hiring the product to do in the context of their actual day. Together they produce a rich, behavior-based picture of the user — not a demographic cartoon.

**Why it fits:** The CPO defines *who the user is* (`/cpo-define`); the CDO goes deeper into *their world and emotions.* This is where "the user is not you" becomes concrete — you map their frustrations, their context, what makes them abandon the product.

**How it powers a command:** Core of `/design-user` — produces 1-2 rich personas, a journey map (before/during/after using the product), and an emotional map (where they feel friction, delight, confusion).

---

### 4. User Flows + Information Architecture + AI Interaction Patterns ★ (How users move through it)

**Source:** Classic IA practice; AI interaction patterns (Anennya, May 5 — original to this project).

**What it is:** A user flow describes the path a user takes to complete a task — first screen, first action, decision points, where they might get stuck. Information architecture is how the whole thing is organized (navigation, structure). The AI-specific layer: how the AI interaction is surfaced (input → loading → output → feedback), and what the user sees when the AI is uncertain.

**Why it fits:** This is the structural heart of UX design — and it's *text-describable*, so Claude can do it well and output prompts for Figma/v0 to render. It's where the AI interaction patterns get designed before anything is built.

**How it powers a command:** Core of `/design-flows` — produces core flow descriptions, a screen list with each screen's purpose, key decision points, navigation structure, and prompts formatted for visual tools. Includes the AI interaction patterns per flow.

---

### 5. Atomic Design + Design Tokens ★ (Keeping it consistent)

**Source:** Brad Frost, *Atomic Design* (2016). The standard methodology for design systems.

**What it is:** Build UIs as a hierarchy — atoms (button, input) → molecules (a search bar) → organisms (a header) → templates → pages. **Design tokens** are the subatomic layer: named values for color, spacing, and type (e.g. `color-brand-blue`) that keep everything consistent. Define the small pieces once, reuse everywhere.

**Why it fits:** Consistency is what makes a solo-built product look professional instead of cobbled-together. Atomic Design gives a beginner a system for it, and tokens output cleanly as Tailwind config / CSS variables / Figma tokens — directly usable.

**How it powers a command:** Core of `/design-system` — produces a design token list (formatted for Tailwind/CSS/Figma), a component checklist (what to build first), and AI-specific component patterns (loading skeletons, confidence indicators, "AI-generated" labels, regenerate buttons). Run *after* the first ~3 flows exist, not before.

---

### 6. Nielsen's 10 Usability Heuristics + the 5-User Rule ★ (Does it actually work?)

**Source:** Jakob Nielsen, Nielsen Norman Group (1994). The most-cited usability standard in the field.

**What it is:** Ten general principles for usable interfaces (visibility of system status, match to the real world, user control, consistency, error prevention, recognition over recall, etc.). The **5-user rule:** testing with just 5 users uncovers ~85% of usability problems — you don't need a big study. Use the **think-aloud protocol** (ask users to narrate as they go).

**Why it fits:** Demolishes the excuse "I can't afford user testing." Five people and a script is enough. The heuristics give a checklist to audit a design against *before* testing, catching obvious problems for free.

**How it powers a command:** Core of `/design-test` — produces a 5-task usability test script, a 3-question post-task interview guide, what to watch for (common failure patterns), and how to feed results back into `/cpo-iterate`. The heuristics double as a self-audit checklist.

---

## What's Intentionally Left Out (And Why)

| Framework | Why we're skipping it |
|---|---|
| **Full WCAG accessibility spec** | Critical, but a deep specialty. Build basic accessibility into `/design-flows` and `/design-system` as defaults rather than a standalone command. Add a dedicated pass later. |
| **Service Blueprinting** | Powerful for complex multi-touchpoint services, but overkill for an MVP. Journey mapping in `/design-user` is enough to start. |
| **Heavy visual design theory (grid systems, color theory deep-dives)** | The AI design tools (v0, Figma AI) handle much of this. The CDO commands focus on structure + briefs, not teaching graphic design. |
| **A/B testing frameworks** | Requires real traffic. Belongs to a later growth/optimization stage, closer to CPO metrics + CMO. |
| **Design ops / multi-designer workflows** | Team-scale. Irrelevant for a solo founder. |

---

## The 5 CDO Sub-Commands — Beginner Question Naming

| Command | Beginner's Question | Track | Framework underneath |
|---|---|---|---|
| **`/design-brand`** | "What should it look and feel like?" | Brand (all tracks) | Brand brief execution (from CMO) + visual identity |
| **`/design-user`** | "Who am I designing for, and what's their world?" | UX | Design Thinking + Empathy Mapping + JTBD-for-UX |
| **`/design-flows`** | "How does someone move through the product?" | UX | User flows + IA + AI interaction patterns |
| **`/design-system`** | "How do I keep the design consistent?" | UX | Atomic Design + design tokens |
| **`/design-test`** | "Does it actually work for real people?" | UX | Nielsen's heuristics + 5-user rule |

**Reads as a sentence:** *Set the look → understand the user → map the flows → systematize what repeats → test with real people.*

---

## How to Actually Run Them — The Step-by-Step Sequence

The two tracks **start in parallel, then converge** (Anennya's model):

```
PARALLEL START:
   /design-brand   ← from /cmo-brandidentity brief   (Brand track — all tracks)
   /design-user    ← from /cpo-define personas        (UX track — apps/workflows)
        ↓
   /design-flows   ← needs the user picture + /cpo-requirements
        ↓
   /design-system  ← needs brand + flows (only after the first ~3 flows exist)
        ↓
   /design-test    ← needs a prototype or live product
        ↓
   feeds → /cpo-iterate (the product loop continues)
```

Two sequencing rules worth calling out:
1. **`/design-brand` and `/design-user` can run at the same time** — one needs the CMO brief, the other needs CPO personas. Neither blocks the other.
2. **`/design-system` comes late on purpose** — you don't build reusable components until you've designed enough flows to know what repeats. Anennya's rule: "after the first 3 flows are defined, not before."

For **consulting-track** founders: run only `/design-brand`. The four UX commands don't apply without a product.

---

## Connection to Other C-Suite Workflows

- **CMO → CDO:** The Brand Identity Brief from `/cmo-brandidentity` is the direct input to `/design-brand`. The voice/tone guide feeds all design copy.
- **CPO → CDO:** User personas from `/cpo-define` feed `/design-user`; user stories/requirements from `/cpo-requirements` feed `/design-flows`.
- **CDO → CPO:** Personas in `/design-user` can validate or challenge `/cpo-define`; `/design-test` results feed `/cpo-iterate`.
- **CDO → CTO:** Finalized flows + component specs from `/design-flows` and `/design-system` are the handoff to the CTO's build (`/cto-mvp`, `/cto-sprint`). Design must finish a flow before it's built.
- **CTO → CDO:** The framework choice from `/cto-stack` affects which component library design can use; the API surface from `/cto-architecture` informs what's possible in `/design-flows`.

---

## Connections — The `/launch` Convergence Command

When `/launch` runs, it pulls these CDO artifacts:

| CDO command output | What `/launch` uses it for |
|---|---|
| `/design-brand` → visual identity | Consistent look across all launch assets (landing page, social, deck) |
| `/design-flows` → finalized flows | Confirms the core experience is designed before users arrive |
| `/design-test` → usability results | Launch gate: did real users succeed at the core task? |
| `/design-system` → component specs | Ensures launch-built screens are consistent, not one-off |

CDO provides the **experience-readiness gate** in `/launch` — for an app/workflow, a product that fails usability testing with 5 users is not launch-ready, no matter how good the tech.

---

## Triggers and Trigger Re-Entry

### When the FULL CDO sequence runs

| Trigger | What just happened | Why the full sequence runs |
|---|---|---|
| **New product / app** | Starting an apps/workflows build | Need brand + user → flows → system → test |
| **New business (any track)** | Starting from zero | At minimum `/design-brand` (brand track applies to all) |
| **Major pivot / rebrand** | `/ceo-pivot` or `/cmo-brandidentity` reset | Brand and/or UX must be reworked |

### When a SUBSET re-fires

| Trigger | What just happened | Commands that re-fire | Why |
|---|---|---|---|
| **Designing a new feature** | Adding to existing product | `/design-flows` (new screens) → `/design-system` (new components if needed) | Brand + user already exist |
| **Users keep getting confused** | Support questions about the same screen | `/design-test` (find the failure) → `/design-flows` (fix it) | Usability problem to diagnose |
| **Product looks inconsistent** | Screens don't match each other | `/design-system` (establish tokens + components) | Consistency gap |
| **Rebrand** | `/cmo-brandidentity` changed | `/design-brand` (re-execute the new brief) | Brand strategy shifted |
| **AI errors confuse users** | Users don't understand AI uncertainty/failures | `/design-flows` (fix AI interaction patterns) | AI experience design gap |
| **Hiring a designer** | Bringing in design help | `/design-system` (the brief they build from) + `/design-brand` | The system/brief is the handoff doc |
| **Quarterly review** | End of OKR cycle | `/design-test` (re-test core flows) | Periodic experience health check |

### Convergence triggers

| Trigger | Commands across roles |
|---|---|
| **Go-to-market launch** | `/design-brand` + `/design-flows` + `/design-test` → experience-readiness gate for `/launch` |
| **Feature launch** | `/cpo-requirements` → `/design-flows` → `/cto-mvp` (build) → CMO announce |
| **Pivot decision** | `/ceo-pivot` → `/design-user` (new) → `/design-flows` (new) |
| **First design hire** | `/design-system` (hand off) + `/cmo-brandidentity` (the strategy context) |

---

## Open Questions / Next Steps

- [ ] Validate with Patty and Anennya
- [ ] Confirm accessibility approach — baked into `/design-flows` + `/design-system` as defaults, vs. a future standalone pass
- [ ] Define the exact prompt format `/design-flows` and `/design-brand` output for Figma / v0 / Canva / Midjourney
- [ ] Decide how `/design-test` recruits 5 users for a pre-launch founder (the chicken-and-egg of testing before you have users)
- [ ] **All 7 roles now defined (CEO, CMO, CRO, COO, CPO, CTO, CDO).** Next: spec the top-level **`/launch` convergence command** and the **shared business brief** (the connective-tissue doc that all commands read/write, holding `founder_technical`, niche, ICP, positioning, pricing, etc.).

---

## Sources

- British Design Council. The Double Diamond (2005). [Double Diamond Design Process — UXPin](https://www.uxpin.com/studio/blog/double-diamond-design-process/)
- Brown, T. *Change by Design*. Harper Business, 2009. (IDEO / Design Thinking.) Stanford d.school five-stage model.
- Gray, D. et al. *Gamestorming* (Empathy Mapping). O'Reilly, 2010.
- Christensen, C.M. et al. *Competing Against Luck* (JTBD). Harper Business, 2016.
- Frost, B. *Atomic Design*. 2016. https://atomicdesign.bradfrost.com/
- Nielsen, J. ["10 Usability Heuristics for User Interface Design"](https://www.nngroup.com/articles/ten-usability-heuristics/). Nielsen Norman Group, 1994. / 5-user rule: ["Why You Only Need to Test with 5 Users"](https://www.nngroup.com/articles/why-you-only-need-to-test-with-5-users/).
- Anennya, *2026_05_05_Brainstorming_C_Suite.md* (WDAI repo). / O'Brien Novak, P., *Phase-1-Frameworks-Patty.md* (WDAI repo).
