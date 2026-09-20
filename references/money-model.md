# Money Model — Quantified ROI Analysis

The workshop's signature feature: every recommendation is translated into
money. This reference defines how. Read it before Stage 1 (to know which
economic baselines to collect) and again before Stage 5 (to build the ROI
section of the report).

## Core Principle

Benefits and costs are expressed in three dimensions, each with a DIFFERENT
calculation method. Never mix them:

1. **Revenue (upside)** — income created or enabled
2. **Cost (savings)** — expenses reduced or avoided
3. **Risk (expected loss)** — probability x impact. Risk is NOT a cost;
   it is an expected value. A 10% chance of losing 50,000 is a 5,000
   expected loss, not a 50,000 cost.

## Required Baselines (collect in Stage 1, confirm before Stage 5)

| Input | Rule |
|---|---|
| Currency | Default USD. Always confirm with the user and let them override. Display all figures in the confirmed currency. |
| Hourly rate of key people | MUST be provided/confirmed by the user in dialogue — never silently assume. If the user is unsure, offer anchors: market salary for their role, or their own billing rate. Record the chosen basis. |
| Fully-loaded hiring cost | For "avoided hire" calculations: salary + benefits + management overhead + ramp time cost. |
| Per-capita output of a hire | What one additional person in that role produces per month (revenue or hours of capacity). |

## The Three Dimensions

### 1. Revenue (upside)

Two forms:

- **Direct revenue lift**: e.g. conversion-rate improvement on an existing
  funnel. Formula: traffic x conversion delta x average order value.
  Require a defensible conversion delta; if none exists, use a scenario
  range (pessimistic / expected / optimistic), never a single point.
- **Capacity redirected to revenue work**: freed hours only count here if
  the user commits to redirecting them to a revenue-generating activity.
  Formula: freed hours x hourly rate x revenue-conversion factor
  (0-100%, user-confirmed — what share of freed time actually goes to
  revenue work). Default factor 50% if the user cannot decide, marked EST.

### 2. Cost (savings)

- **Time savings**: hours saved per year x hourly rate. Per use case.
- **Avoided hires**: roles that would otherwise be hired within 12 months:
  fully-loaded annual cost per role.
- **Avoided rework/external spend**: e.g. reduced contractor revision cycles.

### 3. Risk (expected loss)

For each material risk the AI use case introduces:

expected annual loss = probability (0-1) x impact per occurrence

Common categories: compliance fines (AI-generated ad copy violating
advertising law), platform account penalties, brand damage from
hallucinated customer-facing output, data leakage. Use ranges and mark EST.
Risk reduces net benefit; it does not inflate cost.

## Investment (the denominator)

Annual investment = one-time setup (hours x rate) + tool/API fees per year
+ ongoing maintenance (hours/month x 12 x rate).

## Output Formulas

- Annual gross benefit = revenue + cost savings
- Annual net benefit = gross benefit − expected risk loss
- ROI = (annual net benefit − annual investment) / annual investment
- Payback period (months) = 12 x annual investment / annual net benefit

Always show: the formula, the input values, which inputs are EST, and the
result. A number without its derivation is not allowed in the report.

## Worked Example (USD)

Quick Win: supplier delivery spec pack.
- Cost side: 175 h/yr saved x 200/h = 35,000
- Revenue side: 175 h redirected x 200/h x 50% = 17,500 (EST factor)
- Risk side: 10% x 5,000 brand-risk event = 500 (EST)
- Investment: setup 8h x 200 = 1,600 + tools 100/yr = 1,700
- Net benefit = 35,000 + 17,500 − 500 = 52,000
- ROI = (52,000 − 1,700) / 1,700 ≈ 29.6x  →  payback < 1 month

## Report Requirements

The ROI section of the HTML report must:

1. Present the three dimensions as separate blocks, each with its formula.
2. Make key inputs (currency, hourly rate, hours saved, risk probability)
   user-adjustable where the medium allows, or clearly labeled EST.
3. State the payback period and ROI for each Quick Win and for the
   recommended portfolio as a whole.
4. Include a sensitivity note: which single assumption moves the result most.
