---
name: write-spec
description: "Draft a PRD for a feature or initiative, grounded in your company context. Use when writing a product requirements document, speccing a feature, or documenting requirements for engineering. Produces tiered P0/P1/P2 stories, explicit Non-Goals, and a falsifiable Assumptions table."
---

Follow the `operating-context` protocol first (load company-context.md, check connectors, flag sources).

If the user has not specified a feature, ask: (1) what needs a spec, and (2) what context should be reflected — research, engineering constraints, a customer commitment. If company-context.md defines an active decision, offer it as the default.

Produce a PRD in this format, using the company's vocabulary and named personas throughout:

---

## PRD: [Feature / Initiative Name]

**Author:** [PM persona] | **Status:** Draft | **Last Updated:** [today] | **Target Release:** [infer or TBD]

### Overview
One paragraph: what this does, why now, how it fits the product's positioning.

### Problem Statement
- What is broken or missing today?
- Who is most affected? Use named personas/segments from company context.
- What is the business or customer cost of the current state?
Frame the problem solution-free: "accuracy needs to improve" is a solution wearing a problem costume.

### User Stories (tiered)
**P0 — Must have (release-gating):** … *Acceptance criterion:* …
**P1 — Should have (fast-follow, ~30 days):** … *Acceptance criterion:* …
**P2 — Future (tracked, not committed):** … *Acceptance criterion:* …

3–5 stories total, every story has an acceptance criterion. Be honest about tiers — a P1 that is actually release-gating is a schedule risk hiding in the spec.

### Success Metrics
Tie every metric to a KPI from company context, with current and target values. Include any account-specific SLA commitments.

### Scope
**In scope (goals):** what this release includes.
**Non-goals (explicitly out):** what is deferred, **and why**. Do not soft-pedal deferrals — a stakeholder reading only this section should know exactly what not to expect.

### Assumptions
What this spec believes but has not proven. State each falsifiably:

| Assumption | Evidence today | Risk if false | Validation plan |
|---|---|---|---|

For a deeper pass, run the `assumption-map` skill.

### Technical Constraints
Constraints from engineering (name the owner from company context): timelines, data dependencies, infrastructure, integration complexity. If unknown, flag as an open question.

### Open Questions
Each with an owner and target resolution date. Only genuinely unresolved items — don't list things answerable from context.

---

Close by noting which sections need input before the PRD can be socialized, and offer: run `red-team` on this PRD before it goes to leadership.

---

### Frameworks Behind This Skill
PRD structure per standard product practice (Marty Cagan, *INSPIRED*); Non-Goals and falsifiable-Assumptions sections adapted from marketplace PRD templates (phuryn/pm-skills `create-prd`). P0/P1/P2 tiering per engineering-facing spec convention.
