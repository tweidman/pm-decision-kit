# Pulse KPI Dashboard — Weekly Snapshot (demo data)

## Prediction Quality

| Week | Precision | Recall | Override rate |
|---|---|---|---|
| W-8 | 64% | 71% | 46% |
| W-6 | 66% | 72% | 44% |
| W-4 | 68% | 72% | 42% |
| W-2 | 68% | 73% | 41% |
| Current | 68% | 73% | 41% |

Precision flat for 4 weeks. Model team's last three tuning passes moved precision <1 point each.

## Adoption (beta cohort, 28 CS teams)

- Weekly active CSM users: 62% (target 80%)
- Median early-warning lead time: 31 days (target 45)
- Playbook triggers acted on within 48h: 54%
- Adoption is strongest at accounts where override rate is lowest. Teams with >50% override rates show declining weekly usage — they stop trusting the score and revert to spreadsheets.

## Engineering Notes (David Okafor, last sprint review)

- Precision ceiling attributed to training-data breadth: model trained predominantly on SaaS-vertical accounts; logistics and healthcare verticals underrepresented.
- Closing the gap requires cross-vertical data partnerships or 2–3 quarters of accumulated customer data — not achievable by tuning inside 10 weeks.
- Explainability feature ("why this score") ships in 3 weeks regardless of GA decision.
