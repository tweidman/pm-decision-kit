# Company Context — Veridian Labs (demo)

> Fictional company for evaluating pm-decision-kit. Any resemblance to real companies is coincidental.

## Company & Product

- **Company:** Veridian Labs
- **Product:** Pulse — AI-powered customer health and churn-prediction platform
- **Category / market:** B2B SaaS, customer success technology
- **Stage:** Series C, $52M ARR, ~340 customers
- **One-line positioning:** Pulse predicts which accounts will churn and why — early enough for CS teams to act.

## You (the PM persona)

- **Name / role:** Alex Romano, PM — Pulse Predictions
- **Owns:** the AI churn-prediction module and its GA decision

## Key People

| Name | Role | Relevant because |
|---|---|---|
| Sam Ortega | CEO | Wants the GA recommendation in 72 hours; board review in 10 weeks |
| Lena Fischer | CPO | Alex's boss; socialize recommendations with her first |
| David Okafor | VP Engineering | Owns the model team; says precision ceiling is training-data breadth, not tuning |
| Maya Chen | VP Customer Success | Owns the three strategic-account relationships |

## Accounts That Matter

| Account | Segment | Why they matter |
|---|---|---|
| Hartwell Logistics | Enterprise | $1.8M ARR; GA commitment written into renewal |
| Calder Financial | Enterprise (regulated) | $1.4M ARR; lowest tolerance for wrong predictions |
| Northgate Health | Mid-enterprise | $900K ARR; strong reference account if GA lands |

## KPIs

| Metric | Current | Target | Notes |
|---|---|---|---|
| Churn-prediction precision | 68% | 85% | GA gate; flat for 4 weeks |
| Early-warning lead time | 31 days | 45 days | Improving slowly |
| CSM override rate | 41% | <15% | CSMs re-score accounts manually |
| Weekly active CSM users (beta) | 62% | 80% | Adoption stalls where overrides cluster |

## Competitors

| Competitor | Their strength | Our counter |
|---|---|---|
| RetainIQ | Platform incumbent, broad CS suite, strong brand | Purpose-built prediction depth vs. their bolt-on scoring |
| ClearSignal | Cheap, fast to deploy | Enterprise data integrations and explainable predictions |
| Loyalti | Slick UX, strong mid-market motion | Accuracy at enterprise data scale; security posture |

## Active Decision or Scenario

Pulse churn-prediction precision is at 68% against an 85% GA bar. Three strategic accounts have GA commitments tied to renewals. Sam Ortega wants a ship / hold / hybrid recommendation in 72 hours; board review in 10 weeks. Engineering attributes the precision ceiling to training-data breadth (single-vertical data), not model tuning.

## Vocabulary

health score, churn signal, early-warning lead time, override, playbook trigger, account pulse, signal coverage, CSM (customer success manager)

## Data Sources

- **Project knowledge files:** demo/data/kpi-dashboard.md, demo/data/interview-notes.md, demo/data/launch-brief.md
- **Connected tools:** none (demo runs on files)
