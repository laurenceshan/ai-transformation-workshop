# Industry Scenario Library — Retail & E-commerce

## Industry Snapshot

- Revenue drivers: traffic x conversion rate x basket size x repeat purchase.
  Margin is made in merchandising and supply chain; it is lost in discounting,
  stockouts/overstock, and return handling.
- Common systems: POS/OMS, e-commerce platform (Shopify/Tmall/JD or custom),
  WMS, CRM/membership, ad platform dashboards. Data maturity is usually MEDIUM:
  transactional data is structured and centralized; content, reviews, and
  customer-service text are abundant but unstructured.
- Compliance watchpoints: personal information protection for customer data,
  advertising-claim rules for AI-generated copy, platform rules for automated
  customer contact.

## Value Chain Pain Map

- **Demand/marketing/sales**: ad creative production is slow and expensive;
  campaign copy quality varies by whoever wrote it; channel budgets allocated
  by gut feel.
- **Operations/fulfillment**: demand forecasting by spreadsheet; replenishment
  driven by habit; overstock and stockouts coexist.
- **Customer service**: high ticket volume with 60-80% repetitive questions;
  response quality inconsistent across agents; new agents take months to ramp.
- **Back office**: product listing creation (titles, descriptions, attributes,
  translations) consumes enormous manual hours; reconciliation between
  platforms, payments, and logistics is manual.
- **Management**: daily/weekly reporting is manual screenshot-and-paste;
  promotions evaluated after the fact with no attribution; merchant knowledge
  locked in a few senior buyers' heads.

## Candidate Use Cases

| Use case | Definition (who + what + outcome) | Typical value driver | Typical feasibility concern |
|---|---|---|---|
| CS first-pass drafting | AI drafts replies to customer tickets; agents edit and send | 50-80% of tickets are repetitive; minutes saved per ticket at high volume | Needs ticket history + a maintained knowledge base |
| Product listing generation | Ops staff generate titles, descriptions, attributes, translations from spec sheets | Hours per SKU x catalog size; faster time-to-shelf | Brand tone consistency; ad-law sensitive claims must be filtered |
| Review summarization | Merchandisers read AI digests of reviews/feedback instead of raw text | Faster product iteration; quality issues surface in days not months | Low risk; mostly a prompting + pipeline task |
| Demand forecasting | Planners get AI-assisted SKU-level forecasts to adjust replenishment | Fewer stockouts and less overstock; direct margin impact | Needs clean historical sales data; seasonality/promos make accuracy hard — commonly oversold |
| Ad creative variants | Marketers generate and iterate ad copy/visual variants per channel | More tests per budget dollar; faster creative refresh | Platform review rules; brand consistency |
| Internal knowledge assistant | Staff query SOPs, policies, product info in natural language | Ramps new staff faster; fewer interruptions to senior staff | Knowledge base must actually exist and be maintained — the real work is curation |
| Price/promo analysis | Analysts get AI-prepared post-promo attribution summaries | Better promo ROI decisions next cycle | Attribution is a data-modeling problem first, AI second |
| Return-reason mining | Ops get clustered, quantified return reasons from text + orders | Direct reduction of avoidable returns | Return reasons are often miscoded at the source |

## Common Traps

- **Chatbot before knowledge base**: deploying a customer-facing bot when the
  internal knowledge is scattered — produces hallucinated answers and PR risk.
  Do the internal knowledge assistant first.
- **Forecasting as first project**: demand forecasting is a Big Bet wearing
  Quick Win clothes. Start only after transactional data is verified clean.
- **Fully automated customer contact**: auto-sending AI replies without human
  review; one bad answer to a complaint can cost more than a year of savings.
