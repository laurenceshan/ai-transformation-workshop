# ai-transformation-workshop

An open-source agent skill that turns a general-purpose AI assistant into a
facilitator for **enterprise AI use-case discovery workshops**.

Instead of answering "we should do AI" with generic advice, the skill walks
the user through a structured five-stage interview and produces two concrete
deliverables: a **scored opportunity scorecard** (value x feasibility) and a
**workshop report** with a 90-day action plan.

## What it does

Five stages, one at a time, with a recap and confirmation at each gate:

1. **Business Context** — industry, business model, data/IT maturity, prior
   AI attempts.
2. **Pain Point Collection** — 5-10 pains mapped to processes, each quantified
   in hours, error costs, or revenue at risk.
3. **Use-Case Ideation** — pains converted into candidate use cases, seeded
   by a built-in industry scenario library.
4. **Value x Feasibility Scoring** — anchored 1-5 scoring; feasibility is the
   weakest-link of data / technology / integration / organization. Candidates
   land in four quadrants: Quick Wins, Big Bets, Fill-ins, Money Pits.
5. **Roadmap & Report** — 1-3 Quick Wins to start within 90 days, Big Bets to
   scope next, and an explicit "not now" list.

## Who it's for

- **Executives / business owners** exploring where AI can actually pay off
- **Consultants and FDE-style engineers** who need a repeatable discovery
  method and reusable artifacts
- **IT / digitalization teams** building an AI adoption roadmap

## Usage

Install the skill into your agent environment (any skills-compatible
runtime), then say something like:

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
    ├── industry-template.md          # Template for adding industry libraries
    └── industry-retail.md            # Example library: retail & e-commerce
```

## Contributing

The highest-value contribution is a new **industry scenario library**: copy
`references/industry-template.md`, fill it in for your industry, and open a
PR. See the template for guidelines.

## License

MIT — see [LICENSE](LICENSE).
