# Purpose of CLAUDE.md in the WDAI Toolkit

## Short answer: yes, we need it — for one reason nothing else can replace

**Session-start behavior.** The instruction "when a user opens this project, silently check BUSINESS-BRIEF.md and surface their next step" can only live in CLAUDE.md. Command files only run when invoked. CLAUDE.md loads automatically every session. That's the key difference.

---

## What CLAUDE.md does — and what could live elsewhere

| Purpose | Can it live elsewhere? |
|---|---|
| Session-start routing (check brief, greet, surface next step) | No — only CLAUDE.md auto-loads |
| Routing rules / NL trigger mapping | Partially — command `description` fields handle some of this |
| Tone and persona ("warm business coach") | Could live in each command, but CLAUDE.md makes it consistent |

The routing and persona could theoretically move into each command. But session-start behavior has no other home.

---

## What about members having their own CLAUDE.md?

If members each clone the repo, the CLAUDE.md in the repo becomes their routing brain — and that's fine. It contains behavior instructions, not personal data. All members get the same routing behavior, which is exactly what we want.

The brief (BUSINESS-BRIEF.md) is where personal data lives. That's what's member-specific. CLAUDE.md is the product behavior — it should be the same for everyone.

CLAUDE.md is also scoped to the project directory. Each repo has its own. A member's CLAUDE.md in another project doesn't interfere with this one.

---

## Bottom line

CLAUDE.md is necessary for session-start behavior. It's not configuration — it's the product. Members don't need to touch it. It's the brain; the brief is the memory.
