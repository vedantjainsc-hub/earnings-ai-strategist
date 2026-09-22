---
name: earnings-call-ai-strategy
description: Use when turning earnings materials into a cited AI strategy memo.
version: 1.0.0
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [earnings, sec-filings, ai-strategy, executive-memo, citations]
    related_skills: [grounded-citations, ai-decision-workflow-design, docx, pdf]
---

# Earnings Call to AI Strategy Memo

Produce an auditable **evidence → problem → opportunity → pilot → approval** package for one public company and one completed reporting period.

## Definition of done

A run is complete only when it includes:

- an explicit company identity, ticker, fiscal period, and as-of date;
- the latest available first-party earnings release or remarks, SEC filing, and investor presentation, or a named source gap;
- a source manifest with working URLs;
- exactly three operational problems, each supported by at least one exact quotation;
- fact/inference/assumption labels and at least one limitation or counter-signal per problem;
- AI opportunities mapped to the problems and ranked with visible component scores;
- one 30-day pilot with baseline, target, guardrail, owner role, approval point, and stop condition;
- an executive memo exported as PDF, and DOCX when available;
- a final response that attaches the artifacts and names the three largest caveats.

## Source hierarchy

1. Company investor-relations earnings release, prepared remarks, and official transcript.
2. SEC EDGAR 10-Q or 10-K for the same reporting context.
3. Company investor presentation.
4. Secondary transcript provider only for a documented first-party gap.

Search results and snippets are discovery aids, not evidence. Capture the direct document URL. Record fiscal period and publication date separately.

## Evidence ledger

Maintain a working table with these fields:

| Field | Requirement |
|---|---|
| `claim_id` | Stable identifier such as `P1-E1` |
| `problem` | One of the three selected operational problems |
| `quote` | Exact source substring |
| `speaker_or_section` | Named speaker or filing section |
| `source_title` | Human-readable title |
| `source_type` | Earnings release, remarks/transcript, 10-Q/10-K, or presentation |
| `fiscal_period` | Period the evidence describes |
| `publication_date` | Date the document was published/filed |
| `page_or_anchor` | Page, heading, or transcript segment when available |
| `url` | Direct source URL |
| `interpretation` | Analyst inference, never merged with the quote |
| `limitation` | Missing denominator, management claim, ambiguity, or counter-evidence |

Before quoting, verify the quoted string against extracted source text. If extraction changes typography, shorten to an exact continuous passage rather than silently editing it.

## Selecting the three problems

A problem qualifies when it is operational, material enough to affect an executive decision, repeated or corroborated where possible, and plausibly addressable through a bounded workflow change. Reject generic themes such as “competition,” “uncertainty,” or “growth pressure” unless tied to a named process and evidence.

For each selected problem, write:

1. **Problem statement:** one bounded sentence.
2. **Why now:** evidence from the latest period.
3. **Exact evidence:** quotation, speaker/section, source, date, page/anchor, URL.
4. **Business consequence:** supported fact or clearly labeled inference.
5. **Counter-signal:** evidence that weakens or qualifies the interpretation.
6. **Unknowns:** internal data required before action.
7. **Confidence:** high, medium, or low with rationale.

## Opportunity scoring

Score each component from 1 to 5. Compute:

`weighted_score = 0.35*impact + 0.25*feasibility + 0.25*data_readiness + 0.15*(6-risk)`

Risk is 1 for low risk and 5 for high risk. Use code for arithmetic and display one decimal place. Provide the rationale behind each number; do not score unsupported internal readiness as high. When small reasonable score changes alter the winner, mark the ranking **fragile** and request more evidence.

Every opportunity must specify:

- linked operational problem;
- named user and recurring decision or workflow;
- required inputs;
- bounded output/action;
- human approval point;
- measurable benefit;
- principal failure mode;
- non-AI baseline.

## 30-day pilot contract

Use four one-week phases:

- **Days 1–5 — Validate:** owner interviews, workflow map, data inventory, baseline, privacy/security gate.
- **Days 6–12 — Build:** frozen dataset, baseline method, model-assisted component, review queue, audit fields.
- **Days 13–21 — Test:** offline comparison, error taxonomy, user acceptance, red-team cases.
- **Days 22–30 — Shadow pilot:** no autonomous high-impact action; compare recommendations with current process and produce a go/stop decision.

Required fields:

- decision owner role and frontline user;
- one process and one bounded decision;
- in-scope and out-of-scope;
- required internal data and access approval;
- baseline and target metric with numerator/denominator;
- quality, safety, and adoption guardrails;
- sample-size or case-volume expectation, labeled as an assumption when unknown;
- weekly deliverables;
- human review and escalation path;
- stop condition;
- day-30 decision: stop, extend, or proceed to a controlled production phase.

## Memo production

Use `references/executive-memo-template.md`. Keep the main memo concise enough for an executive to scan; move detailed evidence to an appendix. Create real document artifacts rather than pasting a long chat response. Verify that each artifact opens and that citations and tables are legible before delivery.
