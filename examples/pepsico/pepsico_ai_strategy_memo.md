# PepsiCo — Earnings-to-AI Strategy Decision Memo

**Company:** PepsiCo, Inc.  
**Ticker:** NASDAQ: PEP  
**Fiscal period:** Second quarter and 24 weeks ended June 13, 2026  
**As of:** September 21, 2026  
**Purpose:** Executive operating decision support; not investment advice or equity research.

## 1. Decision requested

**Approve a 30-day, shadow-mode pilot of AI-assisted order-fill exception prioritization in one PepsiCo Foods North America (PFNA) distribution workflow, subject to a five-day data, privacy, and baseline validation gate.**

The pilot should not change orders, inventory allocations, customer commitments, production schedules, or transport plans. It should rank eligible exceptions, copy the evidence behind each ranking, and let an authorized planner accept, reject, or override every recommendation.

## 2. Executive summary

- **Observed operating signal:** Management is explicitly focused on improving PFNA service levels, order fill rates, and unit costs, while also reporting a North American affordability/revenue tension and companywide operating-cost pressure.[1][2]
- **Recommended opportunity:** Give order-fulfillment planners an evidence-backed, ranked exception queue so scarce review time is directed to orders most likely to miss service or fill commitments.
- **Why this pilot now:** It is narrower and safer than automated pricing or autonomous inventory allocation; it connects to named operating metrics and can be tested against historical and shadow-mode outcomes without changing execution.
- **Confidence:** **Medium-low.** Public evidence establishes management priorities, not the existence, frequency, root causes, or financial value of order exceptions. The ranking and all scores are provisional until internal data is inspected.
- **Counter-signal:** PFNA gained volume share and improved household penetration; management did not disclose deteriorating service levels or order fill rates. The proposed pilot therefore tests an opportunity rather than presuming a diagnosed failure.[1][2]

## 3. Company and reporting-period scope

This memo covers PepsiCo, Inc. (PEP) and the latest completed period identified as of September 21, 2026: the 12- and 24-week periods ended June 13, 2026. PepsiCo published its second-quarter release and prepared management remarks on July 9, 2026, and filed the related Form 10-Q on July 9, 2026.[1][2][3]

The analysis uses management statements as claims, not independently verified operating facts. It does not infer confidential systems, datasets, owners, costs, or realized returns.

## 4. Source manifest

| ID | Title | Reporting period | Publication / filing date | Source type | URL | Access date |
|---|---|---|---|---|---|---|
| [1] | PepsiCo Reports Second-Quarter 2026 Results | 12 and 24 weeks ended June 13, 2026 | July 9, 2026 | Company IR earnings release | https://investors.pepsico.com/docs/pepsico-5v9wci20/media/Files/investors/q2-2026-earnings-release.pdf | Sept. 21, 2026 |
| [2] | Second-Quarter 2026 Prepared Management Remarks | Q2 2026 | July 9, 2026 | Company IR prepared remarks | https://investors.pepsico.com/docs/pepsico-5v9wci20/media/Files/investors/q2-2026-prepared-management-remarks.pdf | Sept. 21, 2026 |
| [3] | PepsiCo Quarterly Report on Form 10-Q | 12 and 24 weeks ended June 13, 2026 | Filed July 9, 2026 | SEC filing | https://www.sec.gov/Archives/edgar/data/77476/000007747626000035/pep-20260613.htm | Sept. 21, 2026 |
| [4] | PepsiCo Quarterly Reports | Continuously updated index | Not stated | Company IR earnings index | https://www.pepsico.com/en/investors/earnings | Sept. 21, 2026 |

**Source gaps:** A first-party prepared-remarks document was retrieved and used. PepsiCo’s earnings index listed an investor Q&A transcript, but a stable direct transcript URL was not retrieved for this memo. No separate Q2 2026 investor presentation was identified among the retrieved materials. These gaps reduce confidence in management-context coverage but do not affect the exactness of the quotations used below.

## 5. Three operational problems with exact quotations

### Problem 1 — PFNA must balance affordability actions with net-revenue quality

**Fact:** The earnings release states: “In North America, the convenient foods business gained volume market share aided by innovation and affordability initiatives. Convenient foods net revenue declined and primarily reflects lower effective net pricing.” — *PepsiCo Reports Second-Quarter 2026 Results*, Second-Quarter Results Discussion, page 2, July 9, 2026.[1]

**Inference:** Commercial teams face a recurring decision about which price, pack, promotion, and assortment actions preserve affordability and volume without unnecessarily diluting net revenue. Public evidence does not establish whether the constraint is forecasting, promotion design, retailer execution, mix, or another cause.

**Assumption required to act:** PepsiCo has sufficiently granular, permissioned item/store/customer/channel data, promotion calendars, prices, costs, and outcomes to compare commercial actions on a like-for-like basis.

**Counter-signal / limitation:** Volume market share improved, and management attributes that improvement partly to innovation and affordability. Lower effective net pricing may therefore reflect a deliberate trade-off rather than an execution defect. No public source provides promotion-level profitability or a causal estimate.

**Confidence:** **Medium** that the trade-off is operationally relevant; **low** that AI is the binding solution without internal causal and margin data.

### Problem 2 — PFNA service, fill, and unit-cost improvement requires faster operational exception handling

**Fact:** Prepared remarks state: “we will continue to reduce costs and drive operational excellence – with a focus on ensuring that key metrics such as service levels, order fill rates and costs per unit show improvements.” — Chairman and CEO Commentary, PFNA Highlights, page 7, July 9, 2026.[2]

**Inference:** A plausible bottleneck is the speed and consistency with which planners detect, prioritize, and resolve order-fill exceptions across inventory, production, warehouse, and transport signals. This is a testable inference, not a disclosed PepsiCo diagnosis.

**Assumption required to act:** A meaningful number of eligible exceptions are manually reviewed; their inputs and outcomes are logged; and a planner can intervene before a relevant operational cutoff.

**Counter-signal / limitation:** Management did not report current service levels, order fill rates, unit costs, exception counts, or deterioration. The statement is an improvement objective, not evidence of poor performance.

**Confidence:** **Medium-low**, but it is the most pilotable problem because the cited metrics can be defined and measured without authorizing autonomous action.

### Problem 3 — Operating-cost pressure is partially offsetting productivity gains

**Fact:** The release states: “Core operating profit increased 4%, with core operating margin contracting 40 basis points. The core operating profit performance was primarily driven by productivity savings and effective net pricing, partially offset by certain operating cost increases.” — *PepsiCo Reports Second-Quarter 2026 Results*, Second-Quarter Results Discussion, page 2, July 9, 2026.[1]

**Fact:** The Form 10-Q states: “The 2019 Productivity Plan leverages new technology and business models to further simplify, harmonize and automate processes; re-engineers our go-to-market and information systems, including deploying the right automation for each market; and simplifies our organization and optimizes our manufacturing and supply chain footprint.” — Note 3, 2019 Multi-Year Productivity Plan, printed page 13, filed July 9, 2026.[3]

**Inference:** The transformation portfolio likely requires recurring prioritization of initiatives, dependencies, risks, and realized benefits across markets. A model could help triage evidence and surface inconsistencies, but it cannot establish savings or causal impact.

**Assumption required to act:** Initiative status, milestone, risk, spend, benefit, and dependency data exist in sufficiently standardized and auditable records.

**Counter-signal / limitation:** Productivity savings contributed positively, and restructuring charges were lower year over year. Public evidence does not show that program governance is a bottleneck.

**Confidence:** **Medium** that productivity execution matters; **low** that an AI governance layer would be the highest-value intervention.

## 6. Ranked AI opportunities and transparent scoring

**Formula:** `Weighted score = 0.35×Impact + 0.25×Feasibility + 0.25×Data readiness + 0.15×(6−Risk)`  
Impact, feasibility, data readiness, and risk are scored from 1 to 5. A lower risk score is better; safety is calculated as `6−Risk`. All scores are **provisional** because internal workflow, data-quality, security, and baseline evidence was not available.

| Rank | Opportunity | Linked problem | Impact | Feasibility | Data readiness | Risk | Safety = 6−Risk | Weighted score |
|---:|---|---|---:|---:|---:|---:|---:|---:|
| 1 | Order-fill exception prioritization | Problem 2 | 4 | 4 | 3 | 2 | 4 | **3.75 / 5** |
| 2 | Price-pack-promotion decision support | Problem 1 | 5 | 3 | 3 | 4 | 2 | **3.55 / 5** |
| 3 | Productivity-initiative risk triage | Problem 3 | 3 | 4 | 3 | 2 | 4 | **3.40 / 5** |

### 1) Order-fill exception prioritization — recommended

- **User and decision:** Order-fulfillment or customer-service planners decide which eligible order exception to investigate next before a defined fulfillment cutoff.
- **Inputs:** Order lines, promise dates, available-to-promise inventory, shipment status, substitutions/cancellations, constraints, customer/service tiers, planner notes, and resolved outcomes.
- **Bounded output/action:** Ranked queue with risk reason, copied evidence fields, confidence, and an abstain/review status. No order changes.
- **Human approval point:** Planner accepts, rejects, or reorders each recommendation; only existing authorized systems execute any action.
- **Measurable benefit:** Triage time per eligible exception and recall of genuinely high-priority exceptions before cutoff; secondary monitoring of fill/service outcomes.
- **Principal failure mode:** The model ranks incomplete or stale records, suppressing a critical exception.
- **Non-AI baseline:** Current business rules plus planner-created priority order.
- **Score rationale:** Impact **4** because service, fill, and unit costs are named priorities, but financial value is unquantified. Feasibility **4** because shadow ranking is bounded and reversible. Data readiness **3** because transactional data likely exist, but this is an unverified assumption. Risk **2** only because execution remains human-controlled; risk would rise materially if the tool altered allocation or customer commitments.

### 2) Price-pack-promotion decision support

- **User and decision:** A PFNA revenue-growth-management team selects a small set of price/pack/promotion tests for human review.
- **Inputs:** Item/store/customer/channel sales, net prices, trade spend, costs, promotions, distribution, inventory, competitor observations, and approved constraints.
- **Bounded output/action:** Scenario comparison with uncertainty, comparable historical cases, and exceptions requiring analyst review.
- **Human approval point:** Commercial and finance owners approve any test; the system never changes price or trade terms.
- **Measurable benefit:** Analyst cycle time and forecast calibration on a prospective holdout; not claimed revenue lift.
- **Principal failure mode:** Confounding is mistaken for causality, causing harmful pricing or fairness outcomes.
- **Non-AI baseline:** Existing elasticity models, analyst judgment, and controlled market tests.
- **Score rationale:** Impact **5** because the volume/revenue trade-off is directly cited. Feasibility **3** because causal evaluation and retailer constraints are complex. Data readiness **3** is provisional. Risk **4** because pricing errors can affect consumers, retailers, brand, and regulation even with human review.

### 3) Productivity-initiative risk triage

- **User and decision:** A transformation PMO decides which initiatives need evidence review or escalation each week.
- **Inputs:** Approved initiative register, milestones, dependencies, risks, benefits methodology, status narratives, evidence links, and prior decisions.
- **Bounded output/action:** Evidence-backed exception list for missing proof, inconsistent status, dependency risk, or stale milestones.
- **Human approval point:** PMO owner validates every escalation and benefit claim.
- **Measurable benefit:** Review time, stale-record rate, and precision of escalations accepted by reviewers.
- **Principal failure mode:** Generated summaries create false confidence or misstate realized savings.
- **Non-AI baseline:** Rules for missing fields and standard PMO review.
- **Score rationale:** Impact **3** because the public record does not identify governance as a bottleneck. Feasibility **4** because document and record triage can be run read-only. Data readiness **3** is unverified. Risk **2** if all benefit claims remain evidence-linked and human-approved.

**Sensitivity warning — ranking is fragile.** The lead over opportunity 2 is only 0.20 points. A one-point reduction in order-fill feasibility lowers its score to 3.50, below price-pack-promotion at 3.55; a one-point increase in its risk lowers it to 3.60, nearly erasing the lead. Select the recommended pilot because it is the narrowest reversible test, not because the public-data score implies precision.

## 7. Recommended 30-day pilot

### Pilot contract

**Recurring decision:** Every business day, an authorized PFNA order-fulfillment planner decides which eligible order exception to investigate next using order, inventory, shipment, and constraint evidence, optimizing timely service and fill performance under inventory, operational, privacy, and customer-commitment constraints.

**Decision owner role:** **Assumption to validate:** PFNA supply-chain service / order-fulfillment process owner; exact title and decision rights must be confirmed on Days 1–2.  
**Frontline user:** Authorized order-fulfillment or customer-service planners in one selected operating unit.  
**Scope:** One operating unit or distribution region, one exception type, one daily queue, and one existing resolution workflow selected after the data gate.  
**Out of scope:** Autonomous allocation, order modification, customer communication, production scheduling, route selection, pricing, demand forecasting replacement, workforce decisions, or financial-benefit claims.

### Required data and access approvals

- Order-line ID, item/location, quantity, requested and promised timestamps, service tier, status, and fulfillment outcome.
- Inventory/available-to-promise snapshots and timestamps.
- Shipment, warehouse, production, and transport constraint indicators available to the current planner.
- Planner actions, notes, overrides, resolution timestamp, and reason codes.
- Definition of the operational cutoff and the label for a genuinely high-priority exception.
- Role-based access, data-retention approval, lineage, source timestamps, and a privacy/security review. Customer and employee identifiers should be tokenized or removed unless demonstrably necessary.

### Baseline, target, and measurement contract

**Baseline:** During Days 1–5, measure the current rules-plus-planner workflow on a frozen historical sample and a prospective pre-pilot window:

1. **Median triage minutes per eligible exception** = median of `first-review timestamp − queue-entry timestamp` over all eligible exceptions reviewed.
2. **High-priority recall before cutoff** = number of retrospectively validated high-priority exceptions surfaced before the defined cutoff ÷ total retrospectively validated high-priority exceptions.
3. **False-priority rate** = non-high-priority exceptions placed in the top review band ÷ all exceptions placed in that band.
4. Track service/fill outcomes as contextual outcomes, not causal pilot impact, unless the evaluation design supports attribution.

**Proposed Day-30 target — assumption for executive approval, to be confirmed after baseline:** At least **20% lower median triage minutes per eligible exception** versus the frozen non-AI baseline, while high-priority recall is **no more than 2 percentage points lower** and the false-priority rate is **no more than 5 percentage points higher**. These are pilot acceptance thresholds, not predicted returns.

**Sample-size expectation:** Unknown. The owner must confirm enough eligible cases to evaluate top-band recall and false-priority rate. If fewer than **100 eligible exceptions** or fewer than **20 validated high-priority cases** are available, report descriptive results only and extend or stop; do not claim effectiveness.

### Weekly plan

| Period | Work | Evidence produced | Human approval point |
|---|---|---|---|
| Days 1–5 — Validate | Map current queue and decision rights; select one exception type; inventory fields; freeze eligibility and labels; measure baseline; complete privacy/security gate. | Approved workflow map, data card, baseline report, label rubric, access list, and go/no-go record. | Process owner, data owner, security/privacy reviewer approve before data enters the prototype. |
| Days 6–12 — Build | Implement deterministic rules baseline; create model-assisted ranker with structured reasons, exact source fields, timestamps, confidence, abstention, and audit log. | Reproducible dataset snapshot, rules benchmark, model card, lineage schema, and test results. | Data owner approves snapshot; process owner approves reason codes and review UI. |
| Days 13–21 — Test | Run time-split offline evaluation; compare rules, planner baseline, and hybrid ranker; test stale/missing data, rare exceptions, priority-tier leakage, and adversarial notes. | Error taxonomy, recall/false-priority/cycle-time simulation scorecard, subgroup checks, and red-team log. | Process and risk owners approve or reject shadow deployment. |
| Days 22–30 — Shadow pilot | Display ranked queue beside current workflow; planners follow the current process, record accept/reject/override and reason; no automated action. | Daily audit logs, adoption and override report, matched scorecard, qualitative feedback, and stop/extend/proceed recommendation. | Owner reviews daily safety exceptions and signs the Day-30 decision. |

### Guardrails and human approval

- Use only records an authorized planner may already access.
- Display source fields, source timestamp, rule/model version, confidence, and missing-data warnings.
- Abstain when required fields are missing, stale, contradictory, or outside the approved exception taxonomy.
- Never generate or alter operational facts; reasons must reference copied fields.
- No autonomous action or hidden reprioritization; planners retain the current queue and can ignore the tool.
- Log recommendations, versions, overrides, reasons, and eventual outcomes.
- Review performance by approved operational segment where volumes permit; do not use protected-class attributes.

### Stop conditions

Stop shadow use immediately if: (1) any unauthorized data exposure occurs; (2) the tool writes to an operational system; (3) required lineage or timestamps are missing; (4) high-priority recall is more than 2 percentage points below baseline after the minimum evaluation sample; (5) critical stale-data failures recur after remediation; or (6) planners cannot understand or contest rankings.

**Day-30 decision:**

- **Stop** if safety/data gates fail or no credible workflow bottleneck is confirmed.
- **Extend** if results are directionally useful but the sample is too small or target stability is uncertain.
- **Proceed to a controlled production phase** only if thresholds are met, owners approve, integration remains read-only or separately governed, and a longer causal measurement plan is accepted.

## 8. Risks, assumptions, missing internal evidence, and non-goals

### Principal risks and guardrails

| Risk | Guardrail |
|---|---|
| Stale or incomplete inventory/order data suppresses critical cases | Timestamp checks, required-field validation, abstention, current queue retained |
| Historical planner actions encode inconsistent priorities | Written label rubric, multi-reviewer adjudication, rules baseline, override analysis |
| Model reason sounds plausible but is unsupported | Reasons may cite only copied fields and approved deterministic calculations |
| Local pilot creates customer or service harm | Shadow mode; no operational write; existing planner remains decision maker |
| Apparent service gains are falsely attributed to the pilot | Measure triage outcomes directly; treat service/fill changes as contextual unless design supports causality |
| Sensitive customer or employee data are exposed | Minimize/tokenize identifiers, role-based access, approved retention, audit logs |

### Assumptions to validate

1. Planners manually triage a recurring exception queue before a controllable cutoff.
2. Order, inventory, constraint, review, and outcome timestamps can be joined reliably.
3. A stable high-priority label can be adjudicated without using post-cutoff information in live ranking.
4. One owner has authority over queue policy and pilot stop decisions.
5. The eligible workflow has enough volume for evaluation.

### Missing internal evidence

- Current service level, order-fill rate, cost per unit, and trend by relevant operating unit.
- Exception counts, categories, queue age, review time, and resolution yield.
- Existing rules, optimization, forecasting, and alerting tools; duplication risk.
- Data latency, missingness, label quality, and permissions.
- Economic value per avoided or earlier-resolved exception.
- Planner capacity, adoption constraints, and customer-specific commitments.
- Security, privacy, model-risk, legal, and labor/works-council requirements.

### Non-goals

This memo does not recommend autonomous inventory allocation, dynamic pricing, customer communications, labor decisions, headcount reduction, or a companywide rollout. It does not claim ROI, causal service improvement, data readiness, or that PepsiCo’s current operations are deficient.

## 9. Executive approval checklist

- [ ] Confirm the PFNA process owner and planner users.
- [ ] Confirm one eligible exception type, operating unit, cutoff, and resolution workflow.
- [ ] Approve the data card, access list, retention policy, and privacy/security review.
- [ ] Approve the high-priority label rubric and frozen non-AI baseline.
- [ ] Approve the proposed target and minimum evaluation sample, or replace them before build.
- [ ] Require read-only shadow mode and preserve the current queue.
- [ ] Confirm daily safety review, escalation path, and stop authority.
- [ ] Require Day-30 stop / extend / controlled-production decision with an auditable scorecard.

## 10. Source notes and evidence ledger

| Claim ID | Problem | Exact quotation | Speaker / section | Source, date, page | Interpretation | Limitation |
|---|---|---|---|---|---|---|
| P1-E1 | Affordability vs. net-revenue quality | “In North America, the convenient foods business gained volume market share aided by innovation and affordability initiatives. Convenient foods net revenue declined and primarily reflects lower effective net pricing.” | Second-Quarter Results Discussion | Earnings release, July 9, 2026, p. 2 [1] | Commercial actions involve a volume/value trade-off. | Does not establish causality or an execution defect. |
| P2-E1 | Service/fill/unit-cost execution | “we will continue to reduce costs and drive operational excellence – with a focus on ensuring that key metrics such as service levels, order fill rates and costs per unit show improvements.” | Chairman and CEO Commentary; PFNA Highlights | Prepared remarks, July 9, 2026, p. 7 [2] | These metrics create a measurable pilot boundary. | Objective only; no baseline or deterioration disclosed. |
| P3-E1 | Cost pressure vs. productivity | “Core operating profit increased 4%, with core operating margin contracting 40 basis points. The core operating profit performance was primarily driven by productivity savings and effective net pricing, partially offset by certain operating cost increases.” | Second-Quarter Results Discussion | Earnings release, July 9, 2026, p. 2 [1] | Productivity gains face offsetting cost pressure. | Consolidated result does not identify process-level causes. |
| P3-E2 | Transformation execution | “The 2019 Productivity Plan leverages new technology and business models to further simplify, harmonize and automate processes; re-engineers our go-to-market and information systems, including deploying the right automation for each market; and simplifies our organization and optimizes our manufacturing and supply chain footprint.” | Note 3, 2019 Multi-Year Productivity Plan | Form 10-Q, filed July 9, 2026, printed p. 13 [3] | Transformation is multi-process and multi-market. | Does not show PMO triage is a bottleneck. |

## Sources

[1] https://investors.pepsico.com/docs/pepsico-5v9wci20/media/Files/investors/q2-2026-earnings-release.pdf — PepsiCo Reports Second-Quarter 2026 Results
    > "In North America, the convenient foods business gained volume market share aided by innovation and affordability initiatives. Convenient foods net revenue declined and primarily reflects lower effective net pricing."
    > "Core operating profit increased 4%, with core operating margin contracting 40 basis points. The core operating profit performance was primarily driven by productivity savings and effective net pricing, partially offset by certain operating cost increases."
[2] https://investors.pepsico.com/docs/pepsico-5v9wci20/media/Files/investors/q2-2026-prepared-management-remarks.pdf — Second-Quarter 2026 Prepared Management Remarks
    > "we will continue to reduce costs and drive operational excellence – with a focus on ensuring that key metrics such as service levels, order fill rates and costs per unit show improvements."
    > "We are also elevating productivity across the organization (most notably in developed markets) by advancing our enterprise-wide agenda through automation, digitalization and simplification initiatives across the business that aim to improve operating leverage."
[3] https://www.sec.gov/Archives/edgar/data/77476/000007747626000035/pep-20260613.htm — PepsiCo Q2 2026 Form 10-Q
    > "The 2019 Productivity Plan leverages new technology and business models to further simplify, harmonize and automate processes; re-engineers our go-to-market and information systems, including deploying the right automation for each market; and simplifies our organization and optimizes our manufacturing and supply chain footprint."
[4] https://www.pepsico.com/en/investors/earnings — PepsiCo Quarterly Reports
