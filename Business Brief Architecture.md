# Business Brief Architecture

*Decided June 16, 2026 — based on Opus analysis and team discussion.*

---

## Format: Option B-prime (YAML frontmatter + narrative, two blocks)

Single `business-brief.md` file with frontmatter split into two clearly labeled blocks — business data and journey state — followed by a human-readable narrative.

```markdown
---
# ─── YOUR BUSINESS (you'll rarely touch this) ───
track: product
founder_technical: false
problem_statement: "When X, I want to Y, so I can Z"
niche: "I help [who] with [job]"
icp_seed: "HR directors at mid-size companies..."
product_definition: ""
stack: ""
ai_decisions: ""
pricing_model: ""

# ─── PROGRESS (Claude updates this for you) ───
phase: foundation
current_step: ceo-define-problem
next_step: cpo-define
completed_steps: [start]
current_feature: ""
shipped_versions: []
---

## Your Business Brief

[Human-readable narrative, built up section by section as each command runs.
 This is the part a member actually reads.]
```

---

## Why this format

- **One file, one read** — CLAUDE.md routing checks one file on session start. Fast and reliable.
- **Two blocks separate concerns** — business data rarely changes; journey state updates after every command. Grouping them separately makes frequent state updates cheap and safe.
- **Machine + human readable** — frontmatter gives commands clean named fields to parse; the narrative gives members a document that reads like their business story.
- **Self-healing** — commands rewrite the full frontmatter block from known fields when they save. A member accidentally breaking the YAML gets fixed on the next command run.

### Why not flat markdown (Option A)
Commands need named fields to parse reliably. Flat markdown has no stable extraction point — small member edits silently break extraction.

### Why not modular folder (Option C)
The index drift problem is real: any time you have N source files plus a derived aggregate, the aggregate can desync. The fix requires a regeneration step, ordering conventions, and a git hook — machinery that buys nothing in a single-user, single-project local file. The two-block layout captures Option C's separation benefit without splitting the file.

---

## Where the brief lives: per-project, not global

The toolkit works across repos. Members use it in their meal planner project, their consulting business, their client work — each is a separate context. A single global brief can't serve multiple businesses cleanly.

### The model: global profile + per-project brief

| File | Location | What it holds |
|---|---|---|
| `wdai-profile.md` | `~/.claude/wdai-profile.md` | Who you are — name, track preferences. Written once. |
| `business-brief.md` | `./business-brief.md` (in each project) | What you're building — problem, product, stack, progress. One per project. |

Commands read both. The profile provides member identity so members are never re-asked their name. The project brief holds everything specific to what they're building right now.

### What "adding the toolkit to a project" means

Commands are global (`~/.claude/commands/`). Members install once. When they start working in a new project repo and run their first command, `business-brief.md` is created in that directory automatically. No setup step required.

---

## Field naming (canonical)

`ceo-define-problem` writes `problem_statement` (not `jtbd`). `problem_statement` is plain English — the right choice for the WDAI audience. The MVP spec has been updated to match.

| Field | Written by | Notes |
|---|---|---|
| `track` | `ceo-define-problem` | product / consulting / workflow |
| `problem_statement` | `ceo-define-problem` | canonical — not `jtbd` |
| `niche` | `ceo-define-problem` | one-line niche statement |
| `icp_seed` | `ceo-define-problem` | canonical — not `icp` |
| `phase` | `/start`, `/cto-ship` | coarse lifecycle routing |
| `current_step` | every command | fine-grained routing |
| `next_step` | every command | what CLAUDE.md surfaces next |
| `completed_steps` | every command | full history |

---

## Open items

| Item | Owner |
|---|---|
| Design `wdai-profile.md` format and field list | Patty |
| Confirm commands look for `./business-brief.md` in current directory | Anennya |
| Define the install step — how commands get to `~/.claude/commands/` | Anennya + Patty |
