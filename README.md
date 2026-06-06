# PM Decision Kit

> Nine decision-grade PM skills and one chained launch-decision workflow for Claude Cowork and Claude Code — driven by a single company-context file you fill in once.

Generic AI gives you fluent documents. It doesn't give you better decisions. Most AI-PM tooling stops at "here's your PRD" — what's missing is the discipline around the decision: what are we assuming, what would kill this plan, what does the evidence actually support, and what do we tell the customer when the answer is bad news.

This kit encodes that discipline. Every skill is built around an honest-operator stance: lead with the call, name the cost of the option you recommend, flag inferred data, and never green-light a launch that misses its own success criteria.

## How It Works: Generic Frameworks + Your Context

The skills are deliberately generic — steelman/attack red-teaming, Value/Usability/Viability/Feasibility assumption testing, Tigers/Paper Tigers/Elephants risk triage, current-vs-target metrics scorecards. What makes the output sound like *your company* is one file: `company-context.md`.

Fill in the template once — product, people, KPIs, accounts, competitors, vocabulary — and every skill reads from it. Your PRDs cite your personas, your metrics reviews use your targets, your stakeholder emails name your accounts. Re-skinning the entire kit for a new company or client takes one afternoon, because only the nouns change.

```
your-project/
├── company-context.md        <- copy from templates/, fill in (the only required setup)
└── (your project knowledge: research notes, KPI exports, briefs...)
```

No context file yet? Every skill falls back to the included demo company so you can evaluate the kit out of the box.

## Installation

### Claude Cowork

1. Open **Customize** (bottom-left)
2. **Browse plugins** → **Personal** → **+**
3. **Add marketplace from GitHub**
4. Enter: `tweidman/pm-decision-kit`

### Claude Code (CLI)

```bash
claude plugin marketplace add tweidman/pm-decision-kit
claude plugin install pm-decision-kit@pm-decision-kit
```

Then copy `templates/company-context-template.md` into your project as `company-context.md` and fill it in.

## The Skills

| Skill | What it does |
|---|---|
| `operating-context` | Shared foundation — how every skill loads your company context and uses connected tools (Jira, Slack, Notion, analytics). Not invoked directly. |
| `write-spec` | PRD with P0/P1/P2 tiered stories, explicit Non-Goals, and a falsifiable Assumptions table |
| `roadmap-update` | Quarter view, downstream impact analysis, and internal communication for a roadmap change |
| `metrics-review` | Current-vs-target scorecard, trajectory analysis, root-cause hypotheses, actions with owners |
| `synthesize-research` | Themes, supporting quotes, tensions in the data, and which assumptions the research actually tests |
| `competitive-brief` | Honest competitor strengths, defensible advantages, positioning frame, battle-card lines |
| `stakeholder-update` | Customer, exec, board, and CS-team communications — direct, no hedging, always ends with a next step and owner |
| `assumption-map` | Risky assumptions across Value/Usability/Viability/Feasibility/GTM, prioritized Impact × Evidence, with cheapest tests |
| `red-team` | Adversarial review before a plan meets leadership: steelman → attack, kill criteria, Tigers/Paper Tigers/Elephants, room prep |

**Command:** `/launch-decision` chains five skills — metrics → research → assumptions → red-team → recommendation + stakeholder comms — into one guided ship/hold/hybrid decision workflow. This is the kit's showcase: not "AI wrote a document," but "AI ran a five-step decision with adversarial review built in."

## Try the Demo

The `demo/` folder contains a fictional company — **Veridian Labs**, whose AI customer-health product **Pulse** is below its GA accuracy bar with three enterprise commitments on the line. Copy `demo/company-context.md` into a project along with `demo/data/`, then run:

```
/launch-decision Pulse GA
```

and watch the full decision workflow execute against the demo data.

## Design Principles

1. **Skills are nouns, commands are verbs.** Skills hold single-purpose logic and auto-load when relevant; the command chains them into an end-to-end workflow.
2. **One shared foundation.** Connector behavior and context-loading live in `operating-context`, referenced by every skill — not repeated in each one.
3. **Honesty over polish.** Every skill carries explicit anti-soft-pedaling instructions. A recommendation that hides the cost of its own option is a wish, not a recommendation.
4. **Flag the source.** Outputs distinguish live connector data, project-knowledge data, and inference. An exec will ask "how do you know?" — the answer should already be in the document.
5. **Frameworks are cited.** Each skill ends with the named frameworks behind it, so the kit teaches the method while doing the work.

## Credits

Structure and several patterns adapted from [phuryn/pm-skills](https://github.com/phuryn/pm-skills) (Paweł Huryn, MIT) — notably the marketplace/plugin format, the skills-vs-commands design rule, and elements of the red-team and pre-mortem method. Frameworks credited in each skill: Teresa Torres, Marty Cagan, David J. Bland, Alberto Savoia, Gary Klein, Christina Wodtke, April Dunford, Croll & Yoskovitz, among others.

## License

MIT — see [LICENSE](LICENSE).
