---
name: metrics-review
description: "Analyze product metrics and produce an insight summary. Use when reviewing KPI performance, preparing for a business review or board meeting, investigating a metric gap, or building a data-backed recommendation."
---

Follow the `operating-context` protocol first (load company-context.md, pull live data from Amplitude/Pendo and velocity from Jira/Linear if connected, flag actual vs. assumed numbers).

If the user has not specified metrics, ask: (1) which KPI set, and (2) what decision or audience this is for. Default to the KPIs in company-context.md, prioritizing any tied to an active decision.

Produce:

## Metrics Review: [KPI Set]
**Audience:** [board / exec / team] | **Period:** [infer] | **Prepared by:** [PM persona] | **Date:** [today]

### Current vs. Target
| Metric | Target | Current | Status |
|---|---|---|---|
Use Red / Yellow / Green. Be binary where possible — no "amber" or nuanced language for exec clarity.

### Trend Analysis
For each red or yellow metric: is the gap widening, holding, or closing? At current velocity, when does it hit target? Are there leading indicators suggesting an inflection before the decision date? If the gap is not closable in the available window, say so — and flag whether the target itself needs reconsidering.

### Root Cause Hypothesis
For each red metric: most likely driver, evidence for the hypothesis vs. what's unknown, and the problem class (data quality / model / integration / product design). Name which drivers the engineering owner can actually move in the available window.

### Recommended Actions with Owners
| Action | Owner | Timeline | Expected Impact |
|---|---|---|---|
Be realistic. A recommendation that promises a large metric jump in a short window without engineering backing is not a recommendation — it is a wish. Flag if the gap requires a goal revision rather than a sprint.

### Framing for the Audience
Close with 3–4 sentences that could open the board or exec presentation: acknowledge the gap without apology, show the root cause is understood, communicate a credible path (or an honest conversation about reframing the target), and name the decision to be made and by whom.

---

Close by offering: a `stakeholder-update` for the decision-maker, a `write-spec` for the closing work, or feed this into `/launch-decision` as Step 1.

---

### Frameworks Behind This Skill
Current-vs-target scorecards per standard KPI review practice; root-cause discipline per Lean Analytics (Croll & Yoskovitz) — a metric without a hypothesis about its driver is a vanity number. Target-credibility check per OKR grading practice (Christina Wodtke, *Radical Focus*).
