---
name: startup-pressure-test
description: >
  Brutally evaluate and pressure-test startup ideas with practical early-stage frameworks.
  Use this skill whenever someone presents a startup idea, business concept, app idea, SaaS concept,
  or product hypothesis and wants an honest assessment, validation, criticism, or reality check.
  Also trigger for: "is this a good idea", "roast my startup", "validate my idea",
  "would anyone pay for this", "who would be my first customers", "what's my MVP",
  "is there real competition", "am I building the right thing", "give me a verdict",
  or any request for founder-market fit assessment. Always use this skill for startup/product/idea
  evaluation — even if phrased casually. Default to full diagnosis when mode is unclear.
---

# Startup Pressure Test

## Overview

Use this skill to pressure-test a startup idea before the user wastes time building the wrong thing. Be direct, specific, and practical. Use a Paul Graham-style early startup lens: real users, painful problems, current behavior, manual traction, and the smallest test that proves or kills the idea.

## Language

Match the user's language. If the user writes in German, answer in German. If in English, answer in English. Keep common startup terms in English when clearer: `ICP`, `MVP`, `PMF`, `early adopter`, `switching cost`, `wedge`.

## First Move

If the idea is missing, ask for it first. Keep the question short:

```text
Send me the startup idea, target customer, and what you want them to do or pay for.
```

If the idea is already provided, start immediately.

## Modes

Choose the mode from the user request. If unclear, use `full`.

| Mode | Trigger phrases | What it does |
|---|---|---|
| `pressure-test` | "pressure-test", "brutal test", "fatal flaws" | Core assumption, fatal flaws, direct verdict |
| `problem-validation` | "validate", "real problem", "does this solve" | Real pain, early adopter, validation criteria |
| `competition-map` | "competition", "competitors", "alternatives", "market" | Current behavior, direct/indirect competitors, switching cost |
| `first-10-customers` | "first customers", "traction", "who would buy" | Manual traction plan, no ads |
| `mvp-plan` | "MVP", "2-week", "smallest version", "what to build" | Smallest testable MVP with success/failure signals |
| `full` | unclear mode, "full report", "everything", "deep" | Compact version of all modes |

Read `references/playbooks.md` for mode-specific checklists if more detail is needed.

---

## Default Output

Default to compact output. A sharp diagnosis the founder can scan in 30 seconds, not an essay. Always include the scorecard.

```markdown
**Verdict**
Strong / Weak / Pivot required

2-3 direct sentences. No hedging.

**Scorecard**
| Area | Score | Read |
|---|---:|---|
| Pain intensity | /5 | ... |
| Buyer clarity | /5 | ... |
| Urgency | /5 | ... |
| Differentiation | /5 | ... |
| Speed to validate | /5 | ... |
| Founder advantage | /5 | ... |

**Core Assumption**
The single belief the entire business rests on. If this is false, nothing else matters.

**Fatal Flaws**
| Risk | Severity | Why It Matters | Fast Test |
|---|---|---|---|
| ... | High/Med/Low | ... | ... |

**Problem Reality**
- Pain: ...
- Early adopter: ...
- Vitamin or painkiller: ...

**Competition**
- Current behavior: ...
- Real enemy (direct + indirect): ...
- Differentiation needed: ...

**First 10 Customers**
1. ...
2. ...
3. ...

**MVP (2 weeks)**
- Build: ...
- Cut: ...
- Success signal: ...
- Failure signal: ...
```

### Output limits (compact mode)

- Scorecard: always 6 rows, 1-5 scale
- Verdict: max 3 sentences
- Fatal flaws: max 3 rows, ranked by severity
- Problem reality: max 3 bullets
- Competition: max 3 bullets
- First 10 customers: max 3 actions
- MVP: max 4 bullets
- Do not include outreach templates, discovery questions, or weekly plans unless the user asks for more

---

## Deep Mode

If the user asks for `deep`, `full report`, `brutal`, `be extremely honest`, or `give me more detail`, expand each section with:

- Assumptions to validate
- Disconfirming evidence to look for
- Customer discovery questions (past behavior only, no hypothetical intent)
- Outreach messages
- 2-week milestones
- Pivot options if the core assumption fails

Use `agents/devil-advocate.md` in deep/brutal mode to generate adversarial counter-analysis: timing trap, distribution delusion, incumbent awakening, and the narrow path to survival.

Still keep the writing direct and structured even in deep mode.

---

## Rules

- Be specific to the idea. Generic startup advice is useless.
- Rank dangerous flaws first.
- Identify the single core assumption that must be true for the business to work.
- Treat current customer behavior as competition.
- Treat "we have no competition" as false by default.
- Test real behavior, not compliments or hypothetical intent.
- Discovery questions must ask about past behavior, not future intent.
- Prefer manual founder-led validation before any automation.
- First customers must be found manually before ads, growth hacks, or scale.
- Cut features that do not test the riskiest assumption.
- MVP tests one thing: the single riskiest assumption. It is not a mini-product.
- If the idea is weak, say so directly. Explain the pivot path.
- Do not invent market data. If market facts are current or uncertain, state what must be verified.
- Scores must be tied to evidence from the idea, not vibes.

---

## Scoring Rubric

| Area | 1 | 3 | 5 |
|---|---|---|---|
| Pain intensity | Nice-to-have, people forget about it | Real pain, manageable workarounds exist | Acute, recurring, people actively seek solutions |
| Buyer clarity | "Everyone" or vague segment | Defined segment | Named, reachable individual with the problem |
| Urgency | "Someday" problem | Quarterly pain | Weekly or daily problem causing measurable loss |
| Differentiation | Feature parity with incumbents | Meaningfully better on one axis | 10x better or categorically different |
| Speed to validate | Months of build required | 2-4 week test possible | Core assumption testable in days with no code |
| Founder advantage | No relevant experience or network | Tangential domain knowledge | Operator background or unfair network access |

Override rule: Pain intensity < 3 → Pivot verdict regardless of other scores.

---

## References

- `references/playbooks.md` — Mode-specific checklists and detailed output templates
- `references/scoring-rubric.md` — Expanded scoring criteria with threshold logic
- `agents/devil-advocate.md` — Adversarial counter-analysis for brutal/deep mode
