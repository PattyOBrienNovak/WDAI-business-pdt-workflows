# CLAUDE.md — WDAI AI Business Toolkit

## What This Project Is

Patty O'Brien Novak and Anennya are building a Claude Code toolkit for the 
Women Defining AI (WDAI) community. The goal: give members a set of slash 
commands that walk them through starting and running an AI business — 
whether consulting, building workflows, or developing apps.

Think of it as the business lifecycle equivalent of a developer workflow 
toolkit. Members use slash commands in Claude Code to get real, actionable 
output for their specific business — not generic advice.

## The Audience

WDAI members are business people working to grow their tech fluency. 
Commands should be built for a spectrum:

- **For members:** Plain business language, no assumed technical knowledge, 
  outputs are business artifacts (proposals, pricing docs, client emails, 
  positioning statements). Teach along the way — one sentence of context 
  before, one line of reflection after. Include a "Now share it" promotion 
  moment at every step. At the end of each command output, ask: "Would you 
  like to see the code behind this, or a plain-English explanation of how 
  it works?" — to grow coding comfort at their own pace.
- **For Patty and Anennya:** Show the code behind what's being built. They 
  are coders and want to see and understand the implementation, not just 
  the output.

## Key Reference File

**Phase-1-Consolidated.md** is the research and frameworks foundation for 
everything we build. Read it before working on any command. It contains:
- The 13 universal things everyone needs to figure out when starting an 
  AI business
- Named frameworks for each (Mom Test, StoryBrand, Value-Based Pricing, etc.)
- How each maps to a lifecycle command
- Track-specific notes for consulting, workflows, and apps

## The Lifecycle Commands We're Building

```
/validate  → confirm people will pay before building anything (pre-step)
/discover  → niche + ICP research, competitive landscape
/position  → messaging, offer definition, differentiation
/price     → pricing models, packaging, objection handling
/pitch     → proposals, outreach, follow-up sequences
/deliver   → project and workflow delivery playbook
/operate   → client onboarding, contracts, tools stack
/grow      → case studies, referrals, upsells
/promote   → woven into every command; also standalone
```

## Working in This Repo

- After creating or editing any file, always push to GitHub
- Commands live in `.claude/commands/`
- Keep file names lowercase with hyphens
- Patty and Anennya may work in parallel — pull before pushing
