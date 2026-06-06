---
name: assumption-map
description: "Identify, prioritize, and design tests for the risky assumptions underneath a product decision. Use when a decision rests on beliefs nobody has validated, when the team disagrees on what is true, or when asking whether a target or threshold is even the right one."
---

Follow the `operating-context` protocol first (load company-context.md, pull behavioral evidence from Amplitude/Pendo and research from Notion/Confluence if connected).

If not specified, ask: (1) what decision or plan are we mapping assumptions for, and (2) what evidence already exists. If company-context.md defines an active decision, default to it — including the meta-assumption that its stated target is the right bar.

## Method

1. **Surface assumptions across five risk categories** (don't stop at the obvious ones):
   - **Value** — do users actually behave differently if we deliver this? Is the stated driver the real one?
   - **Usability** — will they use it in-workflow even when it works?
   - **Viability** — do the commercial stakes (contracts, renewals, pricing) actually hinge on what we think they do?
   - **Feasibility** — can engineering deliver inside any commercially relevant window?
   - **Go-to-Market** — is the competitive window real or inflated?

2. **State each assumption falsifiably.** "We believe X. We'll know we're wrong if Y."

3. **Prioritize on an Impact × Evidence matrix.** Impact: how badly does the decision break if this is false? Evidence: how much do we actually have? **High impact + low evidence = test first.** Verdicts: validated / test now / monitor / park.

4. **Design the cheapest test for each "test now."** Prefer skin-in-the-game evidence (what users and accounts *do* — usage data, behavior, contract language) over opinion (what they *say*). For each: hypothesis, method, metric, success threshold, owner, time-box. Tests must fit inside the decision window.

## Output

**Assumption Map: [decision]**
Prepared by: [PM persona] | Date: [today] | Feeds into: […]

### Assumption Inventory
| # | Assumption (falsifiable) | Category | Impact if false | Evidence today | Verdict |
|---|---|---|---|---|---|

### Test Plan (every "test now")
| Assumption | Cheapest test | Metric & threshold | Owner | Time-box |
|---|---|---|---|---|

### What This Changes
2–4 sentences: which assumption, if it fails its test, flips the recommendation — and what the fallback is.

## Key Principle
A target nobody has validated is an assumption wearing a KPI costume. If no one can say where the number came from and what behavior changes at that threshold, the first test is on the target itself.

---

Close by offering: `red-team` to attack the surviving assumptions, or `synthesize-research` to mine existing evidence first.

---

### Frameworks Behind This Skill
Assumption testing across Value / Usability / Viability / Feasibility risks (Marty Cagan, *INSPIRED*; Teresa Torres, *Continuous Discovery Habits*). Impact × Evidence prioritization (David J. Bland, *Testing Business Ideas*). Skin-in-the-game evidence over opinion (Alberto Savoia, *The Right It*).
