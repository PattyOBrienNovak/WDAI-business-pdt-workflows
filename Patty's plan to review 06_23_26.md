# Patty's Plan to Review — June 23, 2026

*Written for async review. Covers the business-brief.md and wdai-profile.md design decisions as of this date, incorporating Anennya's June 16 spec rewrite.*

---

## Context: Where We Are

The MVP-Spec-June-9.md has been significantly rewritten by Anennya (commit `7a1e69c`). Key architectural decisions are now locked:

- **Plugin is definitive** — the toolkit ships as a Claude Code plugin, not a cloned repo
- **SessionStart hook replaces CLAUDE.md routing** — the hook reads the brief on session open and injects routing context; it lives inside the plugin, not in the member's project
- **Field naming resolved** — `problem_statement` and `icp_seed` are canonical (spec and Business Brief Architecture.md now agree)
- **B-prime format confirmed** — YAML frontmatter (two blocks) + human-readable narrative

Two files still need to be created: `business-brief.md` (the template) and `wdai-profile.md` (the global member profile). Both are in the Open Items table in the spec. Both are Patty's ownership.

---

## File 1: `business-brief.md`

### What it is
Per-project file, lives at `./business-brief.md` in each member's project directory. Created automatically on the first command run in a new project. Never set up manually by the member.

### Where it lives
`./business-brief.md` — always in the member's current working directory (`cwd`). The plugin never writes outside this file and `~/.claude/wdai-profile.md`. Commands must always target `cwd` when reading/writing the brief — not the plugin cache.

### The template

```markdown
---
# ─── YOUR BUSINESS (you'll rarely touch this) ───
track: ""
founder_technical: false
problem_statement: ""
niche: ""
icp_seed: ""
product_definition: ""
stack: ""
ai_decisions: ""
pricing_model: ""

# ─── PROGRESS (Claude updates this for you) ───
phase: foundation
current_step: ceo-define-problem
next_step: ""
completed_steps: []
current_feature: ""
shipped_versions: []
---

## Your Business Brief

### The Problem You're Solving
*Written by /ceo-define-problem*

### Validation Signals
*Written by /validate*

### Product Definition
*Written by /cpo-define — updated each time product evolves*

### Current Scope
*Written by /cpo-scope — overwritten each sprint*

### Requirements
*Written by /cpo-requirements — overwritten each sprint*

### User Flows
*Written by /design-flows — overwritten each sprint*

### Build Plan
*Written by /cto-mvp — overwritten each sprint*

### Ship Log
*Written by /cto-ship — appended each release*
```

### Field decisions

**YOUR BUSINESS block — only core fields at creation time:**

| Field | Written by | Notes |
|---|---|---|
| `track` | `/ceo-define-problem` | product / consulting / workflow |
| `founder_technical` | `/start` or `/ceo-define-problem` | calibrates CTO command explanations |
| `problem_statement` | `/ceo-define-problem` | canonical — not `jtbd` |
| `niche` | `/ceo-define-problem` | one-line niche statement |
| `icp_seed` | `/ceo-define-problem` | canonical — not `icp` |
| `product_definition` | `/cpo-define` | added when that command runs |
| `stack` | `/cto-stack` | added when that command runs |
| `ai_decisions` | `/cto-ai` | added when that command runs |
| `pricing_model` | `/cto-pricing` | added when that command runs |

**Fields intentionally NOT pre-populated (added by commands when they run):**
- `validation_status` — added by `/validate`
- `brand_tokens` — added by `/design-brand`
- `framework_used` — experimental only (from the `/test` skill); not in the template until the test skill is proven and adopted

**PROGRESS block — journey state, updated after every command:**

| Field | Purpose |
|---|---|
| `phase` | Coarse routing: foundation / prd / build / shipped / iterating |
| `current_step` | Fine-grained: what's in progress right now |
| `next_step` | What the SessionStart hook surfaces on next session open |
| `completed_steps` | Full ordered history |
| `current_feature` | Set when in the feature loop; cleared after ship |
| `shipped_versions` | History of what shipped and when |

**Per-sprint fields — narrative sections only, NOT in YAML:**
`current_scope`, `current_requirements`, `current_flows`, `build_plan`, `feature_definition` — these are long-form, overwritten each sprint, and too large for YAML. Commands write to the named narrative sections (e.g., `### Current Scope`) instead. Stable headings = reliable read/write without parsing YAML.

**Still open:**
- `signals` field (from `/validate`) — Patty needs to research what this should hold before adding it

---

## File 2: `wdai-profile.md`

### What it is
Global member profile — lives once at `~/.claude/wdai-profile.md`. Created on the member's first command run if not already present. Written once, never needs updating unless something major changes about the member.

### What the spec confirms it must have
From the spec's "What lives where" table and SessionStart hook description:
- `name` — used by the hook for personalized greetings ("Welcome back, Sarah")
- `preferred_track` — used by the hook as a default for new projects that don't have a brief yet

### Proposed full field list

```markdown
---
# ─── WHO YOU ARE ───
name: ""                     # What you'd like to be called
domain: ""                   # Your expertise area (e.g., "HR tech", "healthcare ops", "retail")
technical: false             # true = comfortable reading code; false = plain English
preferred_track: ""          # product | consulting | workflow | "" (leave blank if you do all three)

# ─── HOW YOU LIKE TO WORK ───
explanation_style: teach     # teach = one sentence of context + one line of reflection
                             # direct = skip the pedagogy, just tell me what to do
promote_channel: ""          # Your "Now share it" destination ("LinkedIn", "WDAI Slack", "email list")
show_code_prompt: true       # true = ask "want to see the code?" at end of each command
                             # false = skip that prompt
---

## About You

[Optional — 1–2 sentences about your background and what you're building toward.
 The more context here, the more Claude can tailor examples to your world.
 Example: "I'm an HR consultant with 10 years at enterprise companies, transitioning
 into AI-powered products for the HR space. I prefer concrete examples over theory."]
```

### Field rationale

| Field | Required? | Used by | Why |
|---|---|---|---|
| `name` | Required | SessionStart hook, every command opener | Personalized greetings from the first session |
| `preferred_track` | Required | SessionStart hook (new projects) | Default routing before a brief exists |
| `domain` | Optional | Problem-definition, positioning, pricing commands | Lets commands use domain-specific examples without re-asking |
| `technical` | Optional (default: false) | `/cto-stack`, `/cto-ai`; also `founder_technical` default | `founder_technical` in the project brief overrides this per-project |
| `explanation_style` | Optional (default: teach) | Every command | Powers the teach-along moments; "direct" mode for experienced members |
| `promote_channel` | Optional | End of every command's "Now share it" moment | Personalizes the share prompt ("Post this to [channel]") |
| `show_code_prompt` | Optional (default: true) | End of every command | Controls "Would you like to see the code behind this?" — on by default per CLAUDE.md spec |

**Design rule:** `name` and `preferred_track` are required — a member who fills in only those two gets a fully working experience. The rest tune the experience but have safe defaults.

### Relationship to project brief
`technical` in the profile is a global default. `founder_technical` in `business-brief.md` is a project-specific override. Commands check the project brief first; fall back to profile if not set.

---

## What's Next (Build Order per Spec)

The spec's current build order:

1. **Plugin packaging** — `plugin.json` + `marketplace.json` *(Anennya)*
2. **Business brief + wdai-profile** — the files above *(Patty — this plan)*
3. **SessionStart hook** — reads brief, injects routing context *(Anennya)*
4. **`/start`** — explicit fallback / reset *(Aparna + Patty)*
5. **`/ceo-define-problem`** — ✅ already built
6. **`/cpo-define`** — first iterative command
7. **`/cto-ai`** — highest unique value
8. **`/validate`** — high leverage, lightweight

**Patty's immediate next step:** create the actual `business-brief.md` template file and `~/.claude/wdai-profile.md` file, then push. One open question to resolve first: what does the `signals` field hold (from `/validate`)?

---

## Open Questions (do not build until resolved)

| Question | Owner | Blocks |
|---|---|---|
| What does `signals` hold — a short list? a URL? free text? | Patty (research) | `/validate` command design |
| Should `framework_used` be in the brief once `/test` is proven? | Team | Post-test-skill decision |
| Does `wdai-profile.md` need a `timezone` or `locale` field? | Patty | Potentially useful for scheduled reminders |

---

## Files to Create When Ready

1. `./business-brief.md` — the template in this project repo (as a starter for members to copy, or auto-generated by the plugin)
2. `~/.claude/wdai-profile.md` — global member profile (Patty's own profile as the first real instance)

Both files should be created together, then pushed to GitHub.
