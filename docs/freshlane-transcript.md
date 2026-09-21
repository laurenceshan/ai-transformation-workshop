# Demo Transcript — FreshLane Market (English)

A condensed but faithful simulation of the v3.0 workshop: Stage 0 financial
baseline, five interview stages, tiered number confirmation, relative value
scoring, three-tier ROI. User persona: **Maria Delgado, COO of FreshLane
Market**, a regional grocery chain — 28 stores, $85M annual revenue, 620
employees.

---

## Stage 0 — Financial Baseline

**Skill:** Before we talk about AI, three quick setup questions.

1. **Scope** — are we looking at the whole company or one department?
2. **Precision** — rigorous (line-by-line) or rough (order of magnitude)?
   Either way, every financial figure must come from you or be confirmed by
   you — I will never invent a number.
3. **Attachments** — you can upload financial material (management accounts,
   annual report, a ledger) to speed this up. If you've run this workshop
   before, upload the previous report and we'll verify what changed.

**Maria:** Whole company — I'm the COO. Rigorous mode. Uploading our FY2025
management accounts summary now.

**Skill:** Here's the P&L baseline I extracted. **Please confirm or correct
every line before we use it.**

| Line | FY2025 | Status |
|---|---|---|
| Revenue — grocery (shelf-stable) | $46.0M | ✅ confirmed |
| Revenue — fresh (produce/dairy/meat/bakery) | $24.0M | ✅ confirmed |
| Revenue — pharmacy & services | $9.0M | ✅ confirmed |
| Revenue — other | $6.0M | ✅ confirmed |
| **Total revenue** | **$85.0M** | ✅ confirmed |
| COGS | $63.0M (74%) | ✅ confirmed |
| Labor — store ops / HQ | $11.8M / $2.7M | ✅ confirmed |
| External spend — marketing / IT & services | $1.4M / $1.8M | ✅ confirmed |
| Capital & depreciation | $2.1M | ✅ confirmed |
| Other overhead | $1.4M | ✅ confirmed |
| **EBIT** | **≈ $0.8M (~0.9%)** | ✅ confirmed |

**Skill:** One verdict from this baseline: **you are cost-heavy, not
revenue-constrained.** Margins are grocery-typical thin, so the biggest AI
prizes sit in the cost lines — and inside costs, spoilage/shrink inside COGS
is the largest controllable leak. Your dominant cost category is **labor +
COGS**, so I'll ask headcount-and-hours questions, plus waste questions.

**Maria:** Agreed. Spoilage keeps me up at night.

## Stage 1 — Business Context

**Skill:** Quick context check. Data & systems: is business data centralized?

**Maria:** Centralized POS since 2023, plus an ERP for finance and inventory.
Two years of clean store-level data. But all our *reporting* is still manual
Excel consolidation every Monday.

**Skill:** Prior AI attempts?

**Maria:** We tried a chatbot pilot for HR questions last year. It stalled —
nobody owned it after the vendor demo ended.

**Skill:** Noted — ownership, not technology, killed it. Two baselines the
money model needs. Currency: USD, correct?

**Maria:** Correct.

**Skill:** Hourly rates for the people whose time AI might save. I won't
assume — what are store managers', marketing analysts', and IT's loaded
hourly rates?

**Maria:** Store manager $38/h, marketing analyst $45/h, IT $55/h — all
fully loaded.

*(user-confirmed: currency USD; rates $38 / $45 / $55)*

## Stage 2 — Pain Point Collection

**Skill:** Walking the value chain. Operations first: where do people spend
the most repetitive hours, and where do mistakes cost you money?

**Maria:** Fresh ordering. Every department lead in every store orders by
gut feel, 45–60 minutes a day. And our fresh spoilage is **4.6% of fresh
sales** — the industry good-practice band is around 3%.

**Skill:** 4.6% of $24M = **$1.10M/yr written off** — confirmed? And that's
your number from the accounts, not my estimate.

**Maria:** Confirmed, it's in the upload.

**Skill:** That's P1 — active bleeding, Critical urgency. Next: where else
do hours leak?

**Maria:** Store managers build staff schedules by hand. About **6 hours per
manager per week**, all 28 stores.

**Skill:** 6 h × 28 stores × 52 weeks × $38/h = **$332k/yr of manager time**.
Confirmed as P2. Marketing?

**Maria:** Two analysts, each spending **~10 h/week** pulling promo and trade
numbers into decks.

**Skill:** 20 h/wk × $45 × 52 = **$46.8k/yr** — P3. Anything on the revenue
side?

**Maria:** Our loyalty program covers 41% of sales but we do zero
personalization. I don't know what that's worth — don't guess for me.

**Skill:** I won't. We'll carry it as a candidate with the revenue lift
**pending confirmation** from you. Last one: customer-facing pains?

**Maria:** Service desk answers the same questions all day, but associates
handle it in slack time. Low priority.

**Skill:** Pain map, sorted by urgency:

| # | Pain | Annual bleed | Urgency |
|---|---|---|---|
| P1 | Fresh spoilage, gut-feel ordering | $1.10M | 🔴 Critical |
| P2 | Manual scheduling (mgr time) | $332k | 🟠 High |
| P3 | Manual promo/trade reporting | $46.8k | 🟡 Medium |
| P4 | Zero loyalty personalization | unquantified — pending | 🟡 Medium |
| P5 | Repetitive service-desk questions | slack-time, hard to attribute | 🟢 Low |

**Maria:** Accurate. P1 and P2 are where I'd bet.

## Stage 3 — Use-Case Ideation

**Skill:** Candidates, one sentence each. Tell me accept / reject / adapt.

1. **Fresh demand forecasting** — AI proposes daily order quantities per
   store per fresh category from POS history; department leads review and
   adjust. (from P1)
2. **Scheduling copilot** — AI drafts weekly rosters from forecast footfall
   + availability + labor rules; managers edit and publish. (from P2)
3. **Promo reporting copilot** — AI assembles the weekly trade deck from
   POS/ERP exports; analysts annotate and send. (from P3)
4. **Loyalty personalization** — AI segments loyalty members and drafts
   targeted weekly offers. (from P4)
5. **Service-desk FAQ assistant** — tablet at the desk drafts answers to the
   top recurring questions. (from P5)
6. From the retail library: **fully automated customer email replies** —
   common in retail your size. Relevant?

**Maria:** Accept 1–5. Reject 6 — customer-facing automation without a human
in the loop is not us.

**Skill:** Six → five candidates. Note on #4: loyalty emails are incomplete
for a chunk of members, so expect a data feasibility hit — we'll score it
honestly in Stage 4.

## Stage 4 — Scoring (money first, then value)

**Skill:** Rule: **no value score before the money estimate.** We estimate
each candidate line by line — you supply or confirm every number.

### Candidate 2 — Scheduling copilot

**Skill:** Of the 6 weekly scheduling hours, how many could AI realistically
absorb as a draft you'd review?

**Maria:** Four hours, conservatively three.

**Skill:** Then: expected = 4 h × 28 × 52 × $38 = **$221k/yr**; conservative
= 3 h = **$166k**; optimistic = 5 h = **$277k**. Risk side: mis-scheduled
breaks could trigger labor-compliance fines — what probability and exposure
feel defensible to you?

**Maria:** Say 8% chance of a $12k fine in year one — $960 expected loss.
Tag it as my estimate.

**Skill:** Tagged user-confirmed. Investment: roster tool $24k/yr + setup
120 h IT × $55 = $6.6k + maintenance 4 h/mo ≈ $2.6k → **$33.2k/yr**.
**ROI — conservative 4.0x / expected 5.6x / optimistic 7.4x**; payback
2.4 / 2.1 / 1.7 months. Value score: $221k is 1.5% of your $14.5M labor
line — visible in year-end numbers. That maps to **4**. Agree?

**Maria:** Agree, 4.

**Skill:** Feasibility — data: timeclock + hourly sales in POS → 4.
Technology: drafting rosters is commodity → 5. Integration: standalone tool,
export to your HR system → 4. Organization: managers are drowning and asked
for this → 4. **Feasibility = min(4,5,4,4) = 4. Value 4 × Feasibility 4 →
Quick Win.**

### Candidate 3 — Promo reporting copilot

**Skill:** Of the 20 analyst-hours weekly, how many go away?

**Maria:** Sixteen, conservatively twelve.

**Skill:** Expected 16 h × $45 × 52 = **$37.4k/yr**; conservative **$28.1k**;
optimistic **$42.1k**. Risk is minor — misconfigured data access, 5% × $6k
= $300. Investment: BI copilot licenses $9.6k/yr + setup $3.3k ≈ **$12.9k**.
**ROI — conservative 1.1x / expected 1.9x / optimistic 2.2x.** Value: huge
for one team, invisible at company level → **3**. Agree?

**Maria:** Agree.

**Skill:** Feasibility — data centralized and clean → 4; tech commodity → 5;
integration export-based → 4; analysts eager → 4. **Feasibility 4. Value 3 ×
Feasibility 4 → Quick Win.**

### Candidate 1 — Fresh demand forecasting

**Skill:** Spoilage is 4.6% vs a ~3% good-practice band. What reduction do
you believe is defensible in year one — you tell me.

**Maria:** Getting to 3.9% expected. Conservatively 4.1%, stretch 3.4%.

**Skill:** Then: expected 0.7 pt × $24M ≈ **$168k/yr**; conservative 0.5 pt
= **$120k**; optimistic 1.2 pt = **$288k**. Risk: bad early recommendations
eroding leads' trust — probability × impact?

**Maria:** 25% chance we lose a quarter of adoption → call it $15k impact →
$3.8k expected loss. My estimate, tag it.

**Skill:** Investment: forecasting platform $60k/yr + ERP integration 400 h
× $55 = $22k + change management ≈ **$90k/yr**. **ROI — conservative 0.3x /
expected 0.8x / optimistic 2.2x.** Value score: even the expected tier is
21% of EBIT — company-level needle-mover → **5**. Agree?

**Maria:** Reluctantly agree on 5 — but look at that ROI. First-year
payback is weak.

**Skill:** Exactly why money comes before scoring. Feasibility — data: 2 yrs
clean POS → 4; technology: grocery demand forecasting is proven but
fresh-category accuracy is demanding → 3; integration: cuts into the ERP
ordering workflow → 3; organization: department leads trust their gut —
this is the hard one → 2. **Feasibility = 2. Value 5 × Feasibility 2 →
Big Bet.** Not a 90-day start; it needs a scoped pilot — 3 stores, one fresh
category, 8 weeks, success gate agreed with the leads.

**Maria:** That's honest. Fine.

### Candidate 4 — Loyalty personalization

**Skill:** Revenue lift is yours to state. What would a defensible uplift on
loyalty-attached sales ($31M) be?

**Maria:** I genuinely don't know. Put 0.5% expected, 0.2% conservative, and
mark it pending until our CRM audit.

**Skill:** Tagged **pending confirmation**. Expected ≈ $155k/yr, conservative
$62k. Base value 3; +1 strategic leverage (builds the loyalty data asset) →
**value 4**, stated explicitly. Feasibility — data: 41% penetration,
incomplete emails → 2; technology → 4; integration → 3; organization → 4.
**Feasibility 2. Big Bet** — sequenced behind the CRM data audit.

### Candidate 5 — Service-desk FAQ assistant

**Skill:** Savings hide in slack time and can't be attributed — your words.
Value 2, feasibility 4 → **Fill-in**. Do opportunistically, never prioritize.

**Maria:** Agreed.

### Scorecard

| Candidate | Value | Feasibility | Quadrant | Expected net/yr | ROI (cons/exp/opt) |
|---|---|---|---|---|---|
| Scheduling copilot | 4 | 4 | Quick Win | $220k | 4.0x / 5.6x / 7.4x |
| Promo reporting copilot | 3 | 4 | Quick Win | $37.1k | 1.1x / 1.9x / 2.2x |
| Fresh demand forecasting | 5 | 2 | Big Bet | $164k | 0.3x / 0.8x / 2.2x |
| Loyalty personalization | 4 | 2 | Big Bet | pending | pending |
| Service-desk FAQ | 2 | 4 | Fill-in | ~$0 attributable | — |

## Stage 5 — Roadmap

**Skill:**

- **Start now (≤90 days):**
  1. *Scheduling copilot* — owner: HR ops lead; first step: pick roster tool
     and pilot in 4 stores by week 3. Change note: managers keep final say —
     augmentation, not replacement.
  2. *Promo reporting copilot* — owner: marketing ops; first deck assembled
     by AI in week 2.
- **Scope next:** *Fresh demand forecasting* — 3-store, one-category,
  8-week pilot with a go/no-go gate co-signed by department leads.
  *Loyalty personalization* — blocked until CRM data audit completes.
- **Not now:** service-desk FAQ (fill-in only); fully automated customer
  email (rejected — customer-facing risk).

Portfolio of the two Quick Wins: **net $257k/yr expected ($194k
conservative), ROI 4.2x expected / 3.2x conservative, payback ≈ 2.6 months.**
Sensitivity: the single swing factor is *scheduling hours saved per week* —
every ±1 h moves portfolio ROI by ≈ ±0.9x.

**Maria:** Send me the report.

**Skill:** Assembling the SCORER report — Summary, Context & Pains,
Opportunities, Returns (three-tier, conservative headline, source tags on
every input), Execution, Risks (including the two pending-confirmation
items: loyalty uplift and... nothing else — you confirmed everything else).
