# Scoring Rubric — Value x Feasibility

Score each candidate use case on two axes, 1-5 each. Use the anchors below.
Show the user each score with a one-line justification; the user may adjust.

## Axis 1 — Value (business impact if it works)

Value is scored ONLY AFTER the candidate's financial estimate
(`money-model.md`) is complete and user-confirmed. Anchors are RELATIVE to
the user's own business — the confirmed P&L baseline from Stage 0 — not
absolute thresholds, because the same dollar figure means different things
to a solo business and a listed company.

| Score | Anchor (share of the confirmed business baseline) |
|---|---|
| 5 | Moves the needle on the whole P&L: expected annual benefit is >5% of revenue, or removes a constraint the user has confirmed caps company growth |
| 4 | Material: >1-5% of revenue or of the relevant cost category; the user confirms it would show up in year-end numbers |
| 3 | Meaningful locally: clearly visible to one team or one budget line, but not company-level |
| 2 | Nice-to-have: real but small relative to the business; hard to see in any report |
| 1 | Marginal or symbolic benefit |

Procedure for each candidate:

1. Compute the expected annual benefit from the user-confirmed money-model
   inputs.
2. Express it as a share of the confirmed baseline (revenue for upside cases,
   the relevant cost category for savings cases).
3. Propose the score from the table AND state the importance judgment in
   words ("this touches about 2% of your support cost — that feels like a
   3 to me; do you agree?"). The user confirms both the share and the score.
4. Strategic leverage (data asset creation, capability building) can justify
   +1 — applied at most once per candidate, capped at 5, and stated
   explicitly when used.

## Handling Estimates

Any number not provided or confirmed by the user is an estimate: tag it
"pending confirmation" and list it in the report's Risks section. Before a
use case enters pilot, validate its key baselines (volumes, unit costs); if
actuals differ materially, re-score the candidate before committing build
resources.

## Conditional Feasibility

If feasibility hinges on a prerequisite (e.g. "build the knowledge base
first"), record both scores — current and post-prerequisite — and note the
prerequisite as the first step. Such a candidate can enter the roadmap as a
phase of a related Quick Win rather than a standalone project.

## Axis 2 — Feasibility (can we actually ship it)

Feasibility is the LOWEST of four sub-scores — the weakest link decides:

| Sub-score | Question | 5 looks like | 1 looks like |
|---|---|---|---|
| Data | Does the needed data exist, accessible, usable quality? | Digital, structured, accessible today | Uncollected, on paper, or legally sealed |
| Technology | Is this a solved problem for off-the-shelf AI? | Commodity capability (extraction, classification, drafting, summarization) | Requires research or near-perfect accuracy in a high-stakes domain |
| Integration | Effort to embed into the real workflow? | Standalone tool or single API call into existing system | Touches many core systems, needs process redesign |
| Organization | Will people actually use it? | Pain owner demands it, workflow barely changes | Requires behavior change across departments, or threatens a powerful stakeholder |

## Quadrants

Plot by (value, feasibility):

- **Quick Win**: value >= 3 AND feasibility >= 3.5 — start here
- **Big Bet**: value >= 4 AND feasibility < 3.5 — worth a dedicated feasibility
  study, not immediate build
- **Fill-in**: value < 3 AND feasibility >= 3.5 — do opportunistically, never
  prioritize
- **Money Pit**: value < 3 AND feasibility < 3.5 — say no explicitly

Boundary rule: a candidate scoring exactly 3 on value with feasibility < 3.5
falls outside the four quadrants. Default to **Fill-in**; if it is a
prerequisite for a Quick Win, fold it into that Quick Win's plan instead of
listing it separately. When in doubt, classify conservatively.

## Worked Example

Candidate: "AI drafts first-pass replies to customer service tickets; agents
edit and send."

- Money first: 120 tickets/day x 8 min saved = 16 person-hours/day; at the
  user-confirmed loaded rate this is worth about 4% of the confirmed support
  cost line. User agrees that is material -> Value 4
- Data: 2 years of ticket history in the helpdesk system -> 4
- Technology: drafting replies is a commodity LLM capability -> 5
- Integration: helpdesk has an API; pilot needs no core-system change -> 4
- Organization: agents are overloaded and asked for help; they stay in the
  loop -> 4
- Feasibility = min(4,5,4,4) = 4
- Result: Value 4 x Feasibility 4 -> **Quick Win**
