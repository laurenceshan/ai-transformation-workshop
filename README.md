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

Two guardrails keep the numbers honest:

- **Numbers come from the customer.** Revenue, conversion, pricing, and
  headcount figures are stated by the user, never invented by the AI;
  secondary parameters may be proposed but must be confirmed. Every figure
  in the report carries a source tag.
- **Three-tier ROI.** Every result is shown as conservative / expected /
  optimistic, with the conservative tier as the headline — a single
  optimistic point estimate is a known failure mode.

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

A Stage 0 financial baseline, then five interview stages — one at a time,
with a recap and confirmation at each gate:

0. **Financial Baseline** — role & scope (whole company vs department),
   precision mode (rigorous vs rough), and optional upload of financial
   material (statements, annual reports, ledgers, or a previous workshop
   report). The skill decomposes revenue vs costs into a confirmed P&L
   baseline and delivers one verdict: revenue-constrained or cost-heavy.
   Returning users re-verify changed figures instead of starting over.
1. **Business Context** — industry, business model, data/IT maturity, prior
   AI attempts, plus economic baselines (currency, hourly rates).
2. **Pain Point Collection** — 5-10 pains mapped to processes, each quantified
   in hours and converted to money on the spot, with questioning adapted to
   the cost structure (labor-heavy, external-spend, or capex).
3. **Use-Case Ideation** — pains converted into candidate use cases, seeded
   by a built-in industry scenario library.
4. **Value x Feasibility Scoring** — value is scored only AFTER the financial
   estimate, on 1-5 anchors relative to the user's own business (share of
   revenue or cost affected); feasibility is the weakest-link of data /
   technology / integration / organization. Candidates land in four
   quadrants: Quick Wins, Big Bets, Fill-ins, Money Pits.
5. **Roadmap & Report** — 1-3 Quick Wins to start within 90 days, Big Bets to
   scope next, an explicit "not now" list — and a full three-tier ROI
   analysis.

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
├── SKILL.md                          # Core workflow (Stage 0 + five stages)
└── references/
    ├── financial-baseline.md         # Stage 0: role & scope, precision mode, P&L decomposition
    ├── interview-playbook.md         # Per-stage question scripts & facilitation rules
    ├── scoring-rubric.md             # Relative value anchors, feasibility, quadrants, worked example
    ├── money-model.md                # ROI methodology: confirmation protocol, three tiers, formulas
    ├── industry-template.md          # Template for adding industry libraries
    └── industry-retail.md            # Example library: retail & e-commerce
```

## Contributing

The highest-value contribution is a new **industry scenario library**: copy
`references/industry-template.md`, fill it in for your industry, and open a
PR. See the template for guidelines.

## License

MIT — see [LICENSE](LICENSE).
