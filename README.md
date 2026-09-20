# ai-transformation-workshop

An open-source [agent skill](https://github.com/anthropics/skills) that turns
a general-purpose AI assistant into a facilitator for **enterprise AI use-case
discovery workshops** — and, unlike generic advice, **puts a price tag on
every recommendation**.

Its signature feature is a **quantified ROI model**: each recommended use
case is translated into money across three dimensions — revenue upside, cost
savings, and probability-weighted risk (expected loss, not flat cost) — and
the final interactive HTML report shows ROI, payback period, and a live
calculator where the user can adjust hourly rates, hours saved, and risk
probabilities to stress-test every assumption.

## The SCORER framework

Every workshop report is structured as six sections whose initials spell
**SCORER** — because scoring opportunities is what the workshop does:

- **S**ummary — verdict + top 3 recommendations, with headline ROI figures
- **C**ontext & Pains — business baseline and the urgency-ranked pain map
- **O**pportunities — the value x feasibility scorecard and quadrant grid
- **R**eturns — the ROI analysis with live-adjustable assumptions
- **E**xecution — the 90-day action plan
- **R**isks — risks and open questions, honestly labeled

## What it does

Five stages, one at a time, with a recap and confirmation at each gate:

1. **Business Context** — industry, business model, data/IT maturity, prior
   AI attempts, plus economic baselines (currency, hourly rates).
2. **Pain Point Collection** — 5-10 pains mapped to processes, each quantified
   in hours and converted to money on the spot.
3. **Use-Case Ideation** — pains converted into candidate use cases, seeded
   by a built-in industry scenario library.
4. **Value x Feasibility Scoring** — anchored 1-5 scoring; feasibility is the
   weakest-link of data / technology / integration / organization. Candidates
   land in four quadrants: Quick Wins, Big Bets, Fill-ins, Money Pits.
5. **Roadmap & Report** — 1-3 Quick Wins to start within 90 days, Big Bets to
   scope next, an explicit "not now" list — and a full ROI analysis.

## Who it's for

- **Executives / business owners** exploring where AI can actually pay off
- **Consultants and FDE-style engineers** who need a repeatable discovery
  method and reusable artifacts
- **IT / digitalization teams** building an AI adoption roadmap

## Usage

Install the skill into your agent environment (Claude Code / Kimi / any
skills-compatible runtime), then say something like:

> "Help me figure out where AI can create value in my company."

> "带我做一次AI转型的场景梳理。"

The skill description is written in English; the interview and all
deliverables adapt to the user's language automatically.

## Repository structure

```
ai-transformation-workshop/
├── SKILL.md                          # Core workflow (five stages)
└── references/
    ├── interview-playbook.md         # Per-stage question scripts & facilitation rules
    ├── scoring-rubric.md             # Value x feasibility anchors, quadrants, worked example
    ├── money-model.md                # ROI methodology: revenue / cost / risk formulas
    ├── industry-template.md          # Template for adding industry libraries
    └── industry-retail.md            # Example library: retail & e-commerce
```

## Contributing

The highest-value contribution is a new **industry scenario library**: copy
`references/industry-template.md`, fill it in for your industry, and open a
PR. See the template for guidelines.

## License

MIT — see [LICENSE](LICENSE).
