# Meeting Agenda — June 3, 2026

**Attendees:** Patty, Anennya, Aparna
**Purpose:** Decide the open questions on the C-suite framework toolkit so we can start building commands.

**Context:** All 7 C-suite framework docs are complete, committed, and pushed (CEO, CMO, CRO, COO, CPO, CTO, CDO). Each follows the same shape: beginner role explainer → evergreen frameworks → beginner-question commands → run sequence → cross-role connections → triggers. This meeting is to lock the open decisions.

---

## Sequencing logic

> **Model → Naming → Scope → Brief → Launch → Cleanups.**
> Decide the foundation, then the cross-cutting standard, then what to build first, then the backbone, then the dependent pieces. Highest-leverage and most-debate items first while everyone's fresh; quick confirmations at the end.

**If short on time, protect #2 (naming) and #3 (scope) — those are the real forks in the road. Everything else is mostly confirmation.**

---

## 1. Endorse the overall model *(~10 min — biggest, do first)*

**Decide:** Does the team buy into the parallel C-suite model (7 roles) and the framework selections per role?

- This is the meta-decision. If we want to reshape roles or swap frameworks, everything downstream shifts — so settle it before debating details.
- Builds directly on Anennya's May 5 brainstorm + Patty's Phase 1 research.

**Likely outcome:** Yes, with possible tweaks to specific framework choices.

---

## 2. Command naming convention *(~15 min — cross-cutting standard, blocks all command-building)*

**Decide:** C-suite prefixes + a routing front door, vs. switch to function words.

- Must be decided before anyone authors a command file — it sets the standard for ~43 commands. Changing later = renaming everything.
- **Option A (recommended):** Keep C-suite prefixes (`/ceo-`, `/cmo-`, `/cro-`, `/coo-`, `/cpo-`, `/cto-`, `/design-`) + a plain-English `/start` routing front door that maps intent → role. Preserves the teaching model, stays predictable, turns the acronym barrier into a fluency lesson (WDAI's mission).
- **Option B:** Switch all to function words (`/operate`, `/sell`, `/product`…). More discoverable on first glance, but loses the C-suite teaching frame and several function words are ambiguous (e.g. "execute" fits COO/CTO, not CEO; "grow" collides with the old lifecycle).
- **Note:** `/design-` is already a deliberate exception (CDO is the most obscure title; "design" is unambiguous). If we go Option A, treat `/design-` as the one carve-out, not a precedent.

**This is the item most likely to generate real debate — give it room.**

---

## 3. Scope for the first iteration *(~15 min — turns strategy into a buildable plan)*

**Decide:** What ships first? Which role/commands for the first Build Hour?

- Confirm **CPO/CTO as apps/workflows-only** for this iteration; consulting-lite deferred.
- Confirm **CDO split**: brand track (all tracks) vs. UX track (apps/workflows only).
- **Pick the first 1–2 commands to actually build.** The April 23 review suggested starting with the consulting track + the core early-stage commands (CEO/CMO/CRO). A natural first Build Hour: the CEO "find your bet" commands or CMO `/cmo-positioning`.

**Leave this item with something concrete to build.**

---

## 4. Shared business brief *(~10 min — the backbone the first commands depend on)*

**Decide:** Endorse building it, and align on what fields it holds.

- The connective-tissue document every command reads from and writes to. Without it, the 7 roles are standalone commands instead of a system.
- Candidate fields: `founder_technical` (CTO mode flag), niche, ICP, JTBD, positioning, pricing, track (consulting/workflows/apps), current stage.
- Getting directional input now avoids rework. This is what Aparna will build next regardless.

---

## 5. `/launch` convergence command *(~5 min — depends on brief + roles)*

**Decide / note:** Confirm it's a top-level convergence command; defer the detailed spec until the brief exists.

- Already well-defined by its inputs (every role doc has a "Connections — /launch" section). Lower urgency — just confirm the concept.

---

## 6. Quick confirmations *(~5 min — low-stakes, batch at the end)*

**Confirm:**
- `/cpo-stories` → `/cpo-requirements` rename + the PRD-as-output framing (Anennya's original design — quick nod).
- The `/cmo-brandidentity` (strategy) vs. `/design-brand` (execution) boundary.

---

## Decisions to walk away with

- [ ] C-suite model + frameworks endorsed (or noted changes)
- [ ] Naming convention locked (Option A or B)
- [ ] First 1–2 commands chosen to build
- [ ] Business brief structure agreed
- [ ] `/launch` concept confirmed
- [ ] Rename + boundary confirmations done

---

## Reference — the full command set as it stands

| Role | Commands | Scope |
|---|---|---|
| **CEO** | `/ceo-strategy`, `/ceo-hedgehog`, `/ceo-job`, `/ceo-assumptions`, `/ceo-validate` + `/ceo-pivot`, `/ceo-okrs` | All tracks |
| **CMO** | `/cmo-positioning`, `/cmo-messaging`, `/cmo-brandidentity`, `/cmo-credibility`, `/cmo-audience`, `/cmo-content` | All tracks |
| **CRO** | `/cro-draft-offer`, `/cro-final-offer`, `/cro-pricing`, `/cro-outreach`, `/cro-discovery`, `/cro-pitch`, `/cro-grow` | All tracks |
| **COO** | `/coo-setup`, `/coo-stack`, `/coo-contracts`, `/coo-scope`, `/coo-deliver`, `/coo-getpaid`, `/coo-systemize` (adv) | All tracks |
| **CPO** | `/cpo-define`, `/cpo-scope`, `/cpo-requirements`, `/cpo-metrics`, `/cpo-iterate` | Apps/workflows |
| **CTO** | `/cto-stack`, `/cto-architecture`, `/cto-mvp`, `/cto-sprint`, `/cto-ship`, `/cto-ai`, `/cto-review` (adv) | Apps/workflows |
| **CDO** | `/design-brand` (all tracks), `/design-user`, `/design-flows`, `/design-system`, `/design-test` | Brand=all, UX=apps/workflows |
