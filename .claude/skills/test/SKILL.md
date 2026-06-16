---
name: test
description: EXPERIMENTAL comparison build for /ceo-define-problem. Defines the problem worth solving, but picks the interview framework (Jobs to Be Done vs. The Mom Test) dynamically based on how far along the user already is. Use only to compare against /ceo-define-problem — not the canonical command.
---

# /test — Define the Problem (Dynamic Framework Selection)

This is an experimental version of `/ceo-define-problem`, built to compare a skill+subskill structure against the single-file command. It does the same job — produce a one-page Problem Statement and save it to the shared business brief — but instead of always running the same question set, it picks the right framework for where the user actually is, then reads that framework's file and runs it.

## Step 0 — Check the business brief

Same as `/ceo-define-problem`: if a brief already exists, recap it explicitly and wait for confirmation before continuing. If not, proceed.

## Step 1 — Welcome + what this is

> **What is /test?**
>
> This is an experimental version of the problem-definition step. Instead of one fixed set of questions, it picks the right framework based on where you already are — whether you've talked to real people about this problem, or it's still a hunch.
>
> **Takes about 10 minutes.**

## Step 2 — Pick the framework

Ask one routing question:

> **Have you already talked to people who have this problem, or is this still mostly a hunch?**

- **They've talked to real people / have a customer in mind already:** read `frameworks/jobs-to-be-done.md` and run that flow. JTBD is for sharpening a job you already have signal on.
- **It's still a hunch, they haven't talked to anyone, or their evidence is "I think people would want this":** read `frameworks/mom-test.md` and run that flow. The Mom Test exists specifically to get past polite lies and hypothetical opinions — it's the right tool when there's no real conversation data yet.
- **Unclear from their answer:** ask one gentle follow-up ("Has anyone specifically told you this is a problem for them, or is that an assumption?") before picking.

Tell the user which framework you picked and why, in one line, before starting:

> "Since [reason], I'll use [Framework Name] for this — [one-line description of what that framework does differently]."

## Step 3 — Run the selected framework

Follow the chosen framework file's question flow exactly — one question at a time, reflecting their answer back before the next question, per that file's instructions.

## Step 4 — Synthesize and output the artifact

After the final question, say:

> Great — here's the problem you're solving, in full. Let me pull it together.

Output:

---

**THE PROBLEM YOU'RE SOLVING**
*Draft — [Today's Date] — built using [Framework Name]*

**The core problem, in one sentence:**
> [Core sentence synthesized from their answers]

**What "solved" looks like has three layers:**

| Layer | What they're really after |
|---|---|
| **Functional** | [The practical result] |
| **Emotional** | [How they want to feel] |
| **Social** | [How they want to be seen] |

**Who has this problem**
[1–2 lines from their answers]

**What they do today** (your real competition)
[Current workaround and why it falls short]

**Your niche, in one line**
> I help [who] [solve] [the problem] — so they can [outcome].

---

> **Why [Framework Name]:** [one sentence on why this framework fit their situation, so the comparison with the JTBD-only version is visible]

> **Now share it:** Say your core-problem sentence out loud to one person who fits the customer you described. Watch their face.

> **Your next step is /cpo-define.**

## Step 5 — Save to the brief

Same four fields as `/ceo-define-problem`: `track`, `problem_statement`, `niche`, `icp_seed` — plus one new field for this experimental version: `framework_used` (which framework was selected and why). Confirm: *"Saved to your business brief."*

## Guardrails

- Same guardrails as `/ceo-define-problem` (one question at a time, push toward person/outcome not technology, don't let them skip "what solved looks like").
- **Framework selection is a judgment call, not a quiz.** Don't ask more than one routing question — infer from context where you can.
- This skill is for comparison testing only. Don't suggest it to members as the real command yet.
