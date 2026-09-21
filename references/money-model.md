# Money Model — Quantified ROI Analysis

The workshop's signature feature: every recommendation is translated into
money. This reference defines how. Read it before Stage 0 (to know which
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

## Tiered Number Confirmation (non-negotiable)

ROI hallucination is the skill's most damaging failure mode. Every figure in
a money-model derivation is classified and handled by tier:

- **Critical numbers** — revenue baselines, conversion rates, average order
  value, prices, headcount, salaries/rates, current process volumes. These
  MUST be stated by the user. The facilitator asks; the user answers. The
  facilitator may offer anchors to help the user think (market salary bands,
  their own billing rate) but never fills in the number. A critical number
  the user cannot provide stalls that line of the model — present the
  formula with a blank and move on; do not paper over it.
- **Secondary parameters** — revenue-conversion factor for freed hours, risk
  probabilities, adoption rates. The facilitator MAY propose a defensible
  value with reasoning, but the user must explicitly confirm or adjust it.
  Until confirmed, it is tagged "pending confirmation".
- Every figure in the final report carries a source tag: "user-confirmed" or
  "pending confirmation". Pending items are listed in the Risks section.

Precision mode (chosen in Stage 0) changes how many lines of the model are
built — rigorous mode quantifies every line, rough mode only the dominant
ones — but never relaxes the confirmation rules above.

## Required Baselines (collect in Stage 0/1, confirm before Stage 5)

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
  The conversion delta is a critical number: ask the user what lift they
  believe is defensible; never invent one. If they cannot answer, carry a
  range into the three-tier presentation and mark it pending confirmation.
- **Capacity redirected to revenue work**: freed hours only count here if
  the user commits to redirecting them to a revenue-generating activity.
  Formula: freed hours x hourly rate x revenue-conversion factor
  (0-100%, user-confirmed — what share of freed time actually goes to
  revenue work). If the user cannot decide, propose 50% as a secondary
  parameter and ask them to confirm or adjust.

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
hallucinated customer-facing output, data leakage. Probabilities and impacts
are secondary parameters — propose with reasoning, get user confirmation,
tag unconfirmed ones.
Risk reduces net benefit; it does not inflate cost.

## Investment (the denominator)

Annual investment = one-time setup (hours x rate) + tool/API fees per year
+ ongoing maintenance (hours/month x 12 x rate).

## Output Formulas

- Annual gross benefit = revenue + cost savings
- Annual net benefit = gross benefit − expected risk loss
- ROI = (annual net benefit − annual investment) / annual investment
- Payback period (months) = 12 x annual investment / annual net benefit

Always show: the formula, the input values, the source tag of each input
(user-confirmed / pending confirmation), and the result. A number without
its derivation is not allowed in the report.

## Three-Tier Presentation

A single point estimate of ROI is a known failure mode — it flatters the
case and collapses on first challenge. Present every ROI result in three
tiers, computed from three coherent input scenarios:

- **Conservative**: lowest defensible benefit inputs, highest defensible
  cost inputs. This tier is the DEFAULT headline in the report and executive
  summary.
- **Expected**: the user's own confirmed central estimates.
- **Optimistic**: highest defensible benefit inputs, lowest defensible cost
  inputs. Label clearly; never lead with it.

Each tier shows ROI and payback. If even the conservative tier clears the
user's hurdle, the case is strong; if only the optimistic tier clears it,
say so explicitly.

## Worked Example (USD)

Quick Win: supplier delivery spec pack. (All inputs user-confirmed unless
tagged.)
- Cost side: 175 h/yr saved x 200/h = 35,000
- Revenue side: 175 h redirected x 200/h x 50% = 17,500 (factor proposed
  at 50%, user-confirmed)
- Risk side: 10% x 5,000 brand-risk event = 500 (probability pending
  confirmation)
- Investment: setup 8h x 200 = 1,600 + tools 100/yr = 1,700
- Expected tier: net = 35,000 + 17,500 − 500 = 52,000;
  ROI = (52,000 − 1,700) / 1,700 ≈ 29.6x
- Conservative tier: count cost savings only (no redirect credit), risk
  probability at the pessimistic end 20%: net = 35,000 − 1,000 = 34,000;
  ROI = (34,000 − 1,700) / 1,700 ≈ 19x  → headline figure
- Optimistic tier: redirect factor 70%, risk 5%: net = 35,000 + 24,500 −
  250 = 59,250; ROI ≈ 33.9x

## Report Requirements

The ROI section of the HTML report must:

1. Present the three dimensions as separate blocks, each with its formula.
2. Present every ROI and payback figure in the three tiers
   (conservative / expected / optimistic), with the conservative tier as
   the headline. The executive summary quotes the conservative tier.
3. Tag every input figure as user-confirmed or pending confirmation; make
   key inputs (currency, hourly rate, hours saved, risk probability)
   user-adjustable where the medium allows.
4. State the payback period and ROI for each Quick Win and for the
   recommended portfolio as a whole.
5. Include a sensitivity note: which single assumption moves the result most.
