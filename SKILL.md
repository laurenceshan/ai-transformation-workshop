---
name: ai-transformation-workshop
description: >
  Facilitates a structured, multi-stage AI use-case discovery workshop for
  enterprises. Use this skill whenever a user asks for help with AI
  transformation planning, AI adoption strategy, finding/scoping AI use cases
  for their business, prioritizing AI initiatives, building an AI roadmap, or
  running an AI opportunity assessment. Trigger phrases include: "AI
  transformation", "where can AI help my business", "AI use case discovery",
  "AI roadmap", "AI readiness", "AI opportunity assessment", "prioritize AI
  projects", "数字化转型", "AI转型", "AI落地场景". The skill interviews the
  user stage by stage (business context, pain points, use-case ideation,
  value x feasibility scoring, roadmap), translates every recommendation
  into money (revenue upside, cost savings, probability-weighted risk) and
  produces an interactive HTML report with a full ROI analysis, structured
  as the six-section SCORER framework (Summary, Context & Pains,
  Opportunities, Returns, Execution, Risks).
---

# AI Transformation Workshop

Facilitate a five-stage interview that turns vague "we should do AI" ambition
into a scored, prioritized portfolio of concrete AI use cases and a pragmatic
roadmap.

## Audience

Three user profiles — adapt depth and vocabulary accordingly:

- **Executives / business owners**: talk outcomes, money, risk. Minimal jargon.
- **Consultants / FDE-style engineers**: expect structure, frameworks, artifacts
  they can reuse with clients.
- **IT / digitalization teams**: care about data readiness, integration, effort.

## Core Principles

1. **Business first, technology second.** Every use case must attach to a
   named business process, a pain owner, and a measurable outcome. Reject
   "use LLM somewhere" answers.
2. **Concrete numbers over abstractions.** When quantifying value, substitute
   real figures from the user's business (headcount, ticket volume, hours).
   If unknown, ask; if the user cannot answer, use a clearly-labeled estimate.
3. **One stage at a time.** Do not dump all questions at once. Finish each
   stage, summarize what was learned, get confirmation, then move on.
4. **Language adaptive.** Conduct the interview and write all deliverables in
   the user's own language, even though this skill is written in English.

## Workflow

Run the five stages in order. For the full question scripts and facilitation
tips per stage, read `references/interview-playbook.md` before starting
Stage 1.

### Stage 1 — Business Context

Establish: industry, company size, core business model, main revenue drivers,
current data/IT maturity, any AI attempts so far (and why they failed or
stalled). If the user's industry matches a file in `references/` (e.g.
`industry-retail.md`), load it now — it shapes Stages 2-3.

Also collect the economic baselines (see `references/money-model.md`):
confirm the currency (default USD, user may override), and ask the user for
the hourly rate of key people (founder/team) — never assume it silently.

### Stage 2 — Pain Point Collection

Map the value chain with the user and collect pain points: repetitive manual
work, information bottlenecks, quality/consistency issues, slow decisions,
knowledge locked in people's heads. Aim for 5-10 raw pain points, each tied
to a process and a rough cost (hours/week, error rate, revenue at risk).

### Stage 3 — Use-Case Ideation

Convert pain points into candidate AI use cases. Use the industry scenario
library (if loaded) as seeds — propose library candidates the user has not
mentioned and let them accept, reject, or adapt. Target 6-12 candidates.
Each candidate gets a one-sentence definition: *who* does *what* with AI
assistance to achieve *which outcome*.

### Stage 4 — Value x Feasibility Scoring

Score every candidate on the two axes in `references/scoring-rubric.md`
(read it before this stage). Value: revenue impact, cost saving, time
recovery, strategic leverage. Feasibility: data availability, technical
maturity, integration effort, organizational readiness. Produce a 2x2
classification: Quick Wins / Big Bets / Fill-ins / Money Pits.

### Stage 5 — Roadmap & Report

Recommend a sequence: 1-3 Quick Wins to start within 90 days, 1-2 Big Bets
to scope next, explicit "not now" list. Then produce the HTML report.

## Deliverables

Produce ONE interactive HTML report (self-contained single file), in the
user's language. The report's six sections form the **SCORER framework**:

| Letter | Section | Content |
|---|---|---|
| **S** | Summary | one-paragraph verdict + top 3 recommendations |
| **C** | Context & Pains | business context recap merged into the pain point map |
| **O** | Opportunities | the scored opportunity scorecard |
| **R** | Returns | the ROI / money analysis |
| **E** | Execution | the 90-day action plan |
| **R** | Risks | risks and open questions |

- **Layout**: fixed top navigation listing the six SCORER sections; clicking
  a nav item switches the content panel below. The page itself must never
  show a vertical scrollbar (only a panel may scroll internally if its
  content overflows). The layout must be responsive: desktop first, with
  tablet and phone breakpoints (nav may scroll horizontally, tables may
  scroll inside their own container, multi-column blocks stack to a single
  column) — the no-page-scroll rule holds at every viewport. The footer must
  credit the source repository
  (github.com/laurenceshan/ai-transformation-workshop), its license, and the
  line "Built with the SCORER framework".
- **Summary section**: quote the headline ROI figures (annual net benefit,
  ROI, payback period) with a one-line interpretation, a visible disclaimer
  that all figures derive from estimates agreed during the workshop and are
  not guarantees, and a link that jumps to the Returns section. If the
  report recalculates ROI from adjustable inputs, the Summary figures must
  update in sync.
- **Context & Pains section**: open with a compact business-context recap
  (industry, model, size, data maturity, prior AI attempts), then the pain
  point map. Assign every pain point an urgency level (e.g. Critical / High /
  Medium / Low — define the criteria: rate of time or money bleed x proximity
  to revenue), color-code on a red-to-green scale (red = most urgent), and
  sort the list from most to least urgent.
- **Opportunities section**: table with use case, value score (1-5),
  feasibility score (1-5), quadrant, expected impact in money, first step.
  Sorted by priority. Include the 1-5 anchor definitions for both axes and
  the quadrant definitions, and render the quadrants as a 2x2 grid showing
  where each candidate lands.
- **Returns section** (the signature feature): follow
  `references/money-model.md`. Show revenue, cost, and risk as separate
  blocks with their formulas; make currency, hourly rate, hours saved, and
  risk probability user-adjustable inputs with live recalculation where the
  medium allows; state ROI and payback period per Quick Win and for the
  portfolio.

If the environment cannot render files, fall back to inline markdown with
the same section structure — but the money quantification is not optional.

## Resources

- `references/interview-playbook.md` — per-stage question scripts,
  facilitation rules, and how to handle stuck or over-enthusiastic users.
- `references/scoring-rubric.md` — scoring anchors for value and
  feasibility, weighting, quadrant thresholds, worked example.
- `references/money-model.md` — the ROI methodology: currency and hourly-rate
  baselines, revenue/cost/risk formulas, investment definition, worked
  example, and report requirements.
- `references/industry-template.md` — template for adding a new industry
  scenario library.
- `references/industry-retail.md` — example library: retail & e-commerce.
