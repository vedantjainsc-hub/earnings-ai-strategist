# Earnings to AI Strategist

## From public evidence to one testable AI pilot

**Created by Vedant Jain**

Earnings to AI Strategist is a specialized Hermes agent that turns a public company's latest earnings materials into an evidence-backed AI strategy memo. It identifies three operational problems, ties each one to exact source quotations, ranks bounded AI interventions using a visible scoring model, and proposes one human-reviewed 30-day pilot.

**Watch the demo:** https://youtu.be/HQ1QvQGP5NI  
**Explore the project:** https://github.com/vedantjainsc-hub/earnings-ai-strategist

> The goal is not to generate more AI ideas. The goal is to help an executive decide which operating problem deserves a pilot, what evidence supports it, and what would make the team stop.

## The decision problem

AI opportunity discovery often breaks down before implementation begins:

- Evidence is scattered across earnings releases, SEC filings, presentations, and transcripts.
- Generic ideation produces long lists of use cases with weak links to a workflow, owner, or decision.
- Management claims, analyst interpretation, and unverified assumptions can blur together.
- ROI and data readiness are often implied before internal evidence exists.
- Broad transformation roadmaps make it difficult to learn cheaply or stop early.

This project addresses the front end of AI strategy work. It creates a defensible opportunity hypothesis and a bounded validation plan. It does not replace internal discovery, security review, process mapping, technical architecture, or financial approval.

## What the agent produces

Given an unambiguous public company, the agent produces:

1. A company, fiscal-period, and as-of-date scope.
2. A source manifest built from first-party investor materials and SEC filings.
3. Exactly three operational problems supported by exact quotations.
4. Explicit labels for fact, inference, assumption, counter-signal, and missing evidence.
5. Ranked AI opportunities tied to a user, workflow, decision, required data, and non-AI baseline.
6. One 30-day shadow pilot with a baseline, proposed target, human approval points, guardrails, and stop conditions.
7. An executive decision memo with source links and an approval checklist.

## Evidence-to-decision workflow

```text
Company input
  -> source discovery
  -> source manifest
  -> document extraction
  -> quotation verification and evidence ledger
  -> three operational problems
  -> bounded AI opportunities
  -> transparent scoring and sensitivity check
  -> one 30-day pilot
  -> executive approval memo
```

The output contract is intentionally narrow. A use case cannot appear unless it maps to a source-backed problem. A pilot cannot be recommended unless the use case has a visible evidence trail, an owner, a workflow, a measurement plan, and an explicit score.

## Transparent scoring

Each opportunity receives a 1-to-5 score for:

- Impact: 35%
- Feasibility: 25%
- Data readiness: 25%
- Risk-adjusted safety: 15%

```text
Weighted score =
  0.35 x impact
+ 0.25 x feasibility
+ 0.25 x data readiness
+ 0.15 x (6 - risk)
```

Risk is scored from 1 for low risk to 5 for high risk. The calculation is deterministic and visible. Every component includes a rationale, and the result includes a sensitivity warning. If reasonable changes to inputs reverse the winner, the ranking is labeled fragile.

The score is a decision aid, not proof. Public information cannot establish internal data quality, implementation effort, ownership, operating cost, or realized value.

## The 30-day pilot contract

The selected opportunity becomes a four-stage pilot:

- **Days 1-5: Validate.** Confirm the workflow, owner, internal data, baseline, security requirements, and stop authority.
- **Days 6-12: Build.** Create a frozen-data prototype and a reproducible non-AI baseline.
- **Days 13-21: Test.** Evaluate errors, user acceptance, edge cases, and red-team scenarios.
- **Days 22-30: Shadow.** Run beside the existing process with no autonomous high-impact action.

The day-30 decision is explicit: stop, extend, or proceed to a controlled next phase.

## Case study: PepsiCo

**Public-data demonstration; independent and not endorsed by PepsiCo.**

The analysis examined PepsiCo's Q2 2026 earnings release, prepared management remarks, and Form 10-Q. It identified three operating themes: the affordability and net-revenue trade-off, service/fill/unit-cost improvement, and productivity execution under cost pressure.

The top provisional opportunity was **AI-assisted order-fill exception prioritization** for one PepsiCo Foods North America workflow. The recommended test is read-only and shadow-mode: the system ranks eligible exceptions, copies the evidence behind each ranking, and lets an authorized planner accept, reject, or override every recommendation.

The opportunity scored **3.75/5**, but the ranking was labeled fragile. Public evidence establishes management priorities, not the existence, frequency, root causes, or economic value of order exceptions. The memo therefore recommends a five-day data and baseline gate before any build.

## Case study: JPMorgan Chase

**Public-data demonstration; independent and not endorsed by JPMorgan Chase.**

The analysis examined JPMorgan Chase's Q2 2026 earnings release, presentation, company-published transcript, and Form 10-Q. It focused on AI portfolio prioritization, customer-outcome evidence, and human-controlled workforce transition.

The top provisional opportunity was an **AI use-case evidence and portfolio review assistant** for one non-customer-facing operations portfolio. It would assemble traceable evidence for a monthly human decision to advance, hold, merge, or retire selected use cases. It would not approve funding, deploy models, change controls, make employment decisions, or communicate with clients.

The opportunity scored **4.10/5**. The memo still begins with a stop test: if existing governance already provides timely, complete, evidence-linked reviews, the pilot should not duplicate it.

## Responsible-AI claim discipline

The agent is designed around explicit refusals:

- It does not treat public disclosures as internal truth.
- It does not invent ROI, costs, implementation readiness, or data quality.
- It does not convert management statements into independently verified facts.
- It does not recommend autonomous high-impact action.
- It does not hide missing evidence behind plausible language.
- It does not recommend a companywide transformation from public material alone.

Every recommended pilot keeps a person at the approval point, uses shadow mode before production, records assumptions, and includes stop conditions.

## Technical architecture

The current implementation uses:

- Hermes Agent Bot Mode for the persistent specialist profile.
- A custom system persona for standing behavior and evidence standards.
- A domain-specific skill for source hierarchy, problem selection, scoring, and pilot design.
- Web, browser, and document tools for public research and extraction.
- Code execution for deterministic scoring and consistency checks.
- DOCX and PDF tooling for executive deliverables.
- Persistent profile state for repeated use and future evaluation.

The logical path is deliberately inspectable: sources become evidence records; evidence supports problems; problems produce bounded opportunities; scoring selects one pilot; a human approves or stops it.

## Current status

Completed:

- Working Hermes specialist profile and domain skill.
- Evidence hierarchy, quotation policy, and evidence-ledger structure.
- Transparent opportunity scoring and sensitivity warnings.
- 30-day pilot contract and executive memo template.
- Full public-data demonstrations for PepsiCo and JPMorgan Chase.
- Shareable PDF and editable DOCX memos for both cases.
- Public video demonstration.

Still to validate:

- Practitioner review of evidence quality and recommendation usefulness.
- A human-reviewed benchmark set across sectors.
- Structured SEC ingestion and broader transcript coverage.
- Recommendation consistency across repeated runs.
- Measured adoption, ROI, time savings, or production impact.

## What comes next

1. Have domain practitioners score the case studies using a written rubric.
2. Track quotation accuracy, unsupported-claim rate, ranking stability, pilot completeness, and reviewer disagreement.
3. Add exact-substring quotation tests and fiscal-period consistency checks.
4. Add editable scoring weights and sensitivity visualization.
5. Expand to a third sector and publish what changed after review.
6. Build a lightweight interface only after the decision workflow has demonstrated value.

## Review invitation

The most useful feedback is not whether the interface looks polished. It is whether the evidence supports the problem, whether the scoring assumptions are defensible, and whether the proposed pilot could produce a credible go-or-stop decision.

- Demo: https://youtu.be/HQ1QvQGP5NI
- Repository: https://github.com/vedantjainsc-hub/earnings-ai-strategist
- Case studies: see the `examples/` directory in the repository.

## Disclaimer

This project is an independent demonstration using public information. It is not affiliated with or endorsed by PepsiCo, JPMorgan Chase, or any company analyzed by the agent. It is not investment, legal, accounting, or financial advice. The case-study recommendations are hypotheses for internal validation, not claims about current company operations or production readiness.
