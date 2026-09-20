# Interview Playbook

Per-stage question scripts and facilitation rules. Ask questions one batch at
a time (3-5 per message max), adapt wording to the user's profile, and always
close a stage with a short recap + explicit confirmation before advancing.

## Stage 1 — Business Context

Goal: enough context to anchor every later recommendation.

Ask (adapt to profile):

1. What industry are you in, and what is your core business model — who pays
   you, for what?
2. Rough size: revenue band and headcount. Which teams are largest?
3. Where does the money mainly come from — top 1-2 revenue drivers?
4. Current state of data and systems: do you have ERP/CRM/POS or equivalent?
   Is business data centralized or scattered across spreadsheets and chat
   threads?
5. Have you tried AI before? What happened — and why did it stall or fail?

Economic baselines (required — the money model depends on them):

6. Currency for all figures: default USD, but confirm and let the user
   override.
7. Hourly rate of the key people whose time the use cases will save (founder,
   team leads). Ask directly; never assume silently. If the user is unsure,
   offer anchors (market salary for the role, or their billing rate) and
   record which basis was chosen.

Facilitation tips:

- If the user is vague ("we do everything"), force a choice: "If you could
  only keep one revenue line, which would it be?"
- Note the industry. If a matching `industry-*.md` exists in this directory,
  load it before Stage 2.
- If the user cannot answer the data question, that itself is a finding:
  record data maturity as LOW.

## Stage 2 — Pain Point Collection

Goal: 5-10 raw pain points, each tied to a process and a rough cost.

Walk the value chain with the user (adjust to their industry):

- Demand side: marketing, sales, customer acquisition
- Operations: production, fulfillment, service delivery
- Support: customer service, after-sales
- Back office: finance, HR, procurement, compliance
- Management: reporting, decision-making, knowledge transfer

For each area, ask: "Where do people spend the most repetitive hours? Where
do mistakes or delays cost you money? What knowledge lives only in specific
people's heads?"

Quantify each pain point with concrete numbers, and convert hours into money
immediately using the confirmed hourly rate:

- "How many people, how many hours per week?" — then say what that is worth
  per year in the confirmed currency.
- "What does an error cost? How often?"
- "What would it cost to hire someone to absorb this work instead?"
  (fully-loaded cost + ramp time — needed for avoided-hire calculations)
- If unknown: agree on a clearly-labeled estimate.

Facilitation tips:

- Reject abstract pains ("communication is inefficient"). Drill until you
  get a scene: who, doing what, how often, costing how much.
- Watch for pains that are actually process problems, not AI problems. Record
  them but flag them honestly.

## Stage 3 — Use-Case Ideation

Goal: 6-12 candidate use cases, each defined in one sentence:
*who* does *what* with AI assistance to achieve *which outcome*.

Method:

1. Convert each Stage 2 pain point into 1-2 candidate use cases.
2. If an industry library is loaded, propose 2-4 library candidates the user
   has not mentioned. Present them as hypotheses: "Retailers your size often
   use AI for X — relevant to you?"
3. Merge duplicates; drop anything the user explicitly rejects.

Rules:

- Every candidate must trace back to a pain point or an accepted library
  hypothesis. No orphan ideas.
- Prefer augmentation ("AI drafts, human approves") over full automation for
  candidates touching customers or money — flag the risk difference.

## Stage 4 — Scoring

Read `scoring-rubric.md` and score each candidate on value and feasibility.
Show the user the scores and rationale; let them challenge and adjust. The
user owns the final scores.

## Stage 5 — Roadmap

From the scorecard, recommend:

- **Start now (<=90 days)**: 1-3 Quick Wins. For each: scope, owner, first
  concrete step, expected impact in numbers, a rough budget band (tools +
  integration + internal time), and a one-line change-management note — who
  is affected and how to position it (augmentation, not replacement).
- **Scope next**: 1-2 Big Bets worth a deeper feasibility study.
- **Not now**: explicit list with one-line reasons. This list builds trust.

Then assemble the HTML report described in SKILL.md. Before writing the ROI
section, re-read `references/money-model.md` and confirm its baselines
(currency, hourly rate) with the user if they were not fixed in Stage 1.

## Handling Difficult Situations

- **User wants to skip stages**: allow it, but mark skipped-stage findings as
  assumptions in the report.
- **User wants everything at once**: explain that scoring without pain
  quantification produces fantasy rankings; offer a fast-track version
  (Stages 1+2 combined, single batch of questions).
- **User expects tool/vendor recommendations**: stay tool-agnostic in scoring;
  vendor selection belongs to the follow-on feasibility study of the top
  Quick Win.
