---
description: Run the full launch decision workflow — metrics, research, assumptions, adversarial review, recommendation, and stakeholder communication
argument-hint: "<release or feature, e.g. 'Pulse GA'>"
---

# /launch-decision — The Full Ship/Hold/Hybrid Decision

Chain five skills into one guided decision workflow for $ARGUMENTS. This is not a report generator — it is a guided decision. Follow the `operating-context` protocol throughout; each step inherits the honesty rules.

## How to Run It

Announce the five steps up front. After each step, give a one-line progress label ("Step 2 of 5 — research synthesis") and let the user redirect before continuing. The user can enter at any step ("just run the red-team") — don't gate them.

### Step 1 — Where do the numbers actually stand?
Apply the `metrics-review` skill: current vs. target for the release-gating KPIs. Trajectory call: does any realistic path hit the bar inside the window, or not?

### Step 2 — What does the qualitative evidence say?
Apply the `synthesize-research` skill: what user research says about what the current state costs in practice and what threshold actually changes behavior. Carry forward the strongest 2–3 findings, not the full synthesis.

### Step 3 — What are we assuming?
Apply the `assumption-map` skill, abbreviated: the 3–5 load-bearing assumptions under the decision, each with a verdict (validated / test now / monitor). Always include the meta-assumption: is the stated target the right bar?

### Step 4 — Attack the draft recommendation.
Form the draft call — ship / hold / hybrid — then apply the `red-team` skill against it: top kill-assumptions, Tigers vs. Paper Tigers vs. Elephants, what to verify in the remaining window, and the hardest questions the decision-maker will ask.

### Step 5 — The recommendation and the communication.
Produce the final output:

**Launch Recommendation: [release]**
Prepared by: [PM persona] | For: [decision-maker] | Date: [today]

1. **The call** — one line, first sentence: ship / hold / hybrid, with the date or condition attached.
2. **Why** — 3–5 evidence bullets from Steps 1–3, each tagged with its source (live data / project knowledge / inference).
3. **What survived red-team** — the risks accepted with eyes open, and the kill criteria that would change the call.
4. **The cost of this option** — named plainly, including impact on the accounts that matter.
5. **Next actions** — owner and date for each, inside the decision window.

Then offer the `stakeholder-update` skill for the affected accounts and the internal version for leadership.

## Principles
- If a step's conclusion contradicts an earlier step, surface the contradiction — that tension *is* the decision.
- Do not green-light a launch that misses its own success criteria. If the evidence says hold, say hold, and make the alternative credible.
