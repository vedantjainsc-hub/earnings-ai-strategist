# Earnings → AI Strategist

A shareable [Hermes Agent](https://github.com/NousResearch/hermes-agent) profile that turns public-company earnings materials into cited AI opportunity memos and 30-day pilot plans.

## Watch and read

- [Watch the video demonstration](https://youtu.be/HQ1QvQGP5NI)
- [Download the reader-facing project overview](docs/Earnings_AI_Strategist_Project_Overview.pdf)
- [Read the accessible Markdown overview](docs/project-overview.md)

## Published case studies

| Company | Reporting context | Recommended pilot hypothesis | Artifacts |
|---|---|---|---|
| PepsiCo | Q2 2026 | Shadow-mode order-fill exception prioritization in one PFNA workflow | [PDF, DOCX, Markdown, and evidence ledger](examples/pepsico/) |
| JPMorgan Chase | Q2 2026 | AI use-case evidence and portfolio review assistant for one non-customer-facing operations portfolio | [PDF, DOCX, Markdown, and evidence ledger](examples/jpmorgan-chase/) |

Both analyses are independent demonstrations using public information. They are not affiliated with or endorsed by the companies, and their recommendations require internal validation.

## What it does

Given a company name or ticker, the agent:

1. identifies the latest completed reporting period;
2. collects first-party earnings materials, the relevant SEC filing, and the investor presentation;
3. selects exactly three operational problems supported by exact quotations;
4. separates sourced facts, analyst inference, and unverified assumptions;
5. ranks bounded AI opportunities by impact, feasibility, data readiness, and risk;
6. proposes one human-reviewed 30-day pilot;
7. exports an executive decision memo.

The system is a strategy hypothesis generator. It is not investment advice, an equity-research product, or a substitute for internal discovery.

## Decision workflow

```text
Company input
  → source manifest
  → document extraction
  → quotation verification and evidence ledger
  → three operational problems
  → bounded AI opportunities
  → transparent scoring and sensitivity check
  → 30-day pilot
  → executive approval memo
```

## Install

Install [Hermes Agent](https://hermes-agent.nousresearch.com/docs/getting-started/installation), then run:

```bash
hermes profile install github.com/vedantjainsc-hub/earnings-ai-strategist --alias
```

Start the agent:

```bash
earnings-strategist chat
```

Each installer supplies their own model credentials and web-research configuration. The distribution does not include API keys, credentials, memories, or sessions.

## Example prompt

```text
Analyze PepsiCo and produce the latest earnings-to-AI strategy memo.
Use first-party investor materials and the relevant SEC filing.
Show exact supporting quotations, score the opportunities transparently,
and recommend one 30-day pilot. Treat internal-data assumptions as unverified.
```

## Scoring method

```text
weighted score =
  0.35 × impact
+ 0.25 × feasibility
+ 0.25 × data readiness
+ 0.15 × (6 − risk)
```

All components use a 1-to-5 scale. Risk is 1 for low risk and 5 for high risk. Scores must include a rationale. A ranking is labeled fragile when reasonable changes to assumptions or weights reverse the winner.

## Repository contents

- `SOUL.md`: the bot's standing role and behavior.
- `skills/ai-strategy/earnings-call-ai-strategy/SKILL.md`: the reusable analysis workflow.
- `skills/ai-strategy/earnings-call-ai-strategy/references/executive-memo-template.md`: the memo structure.
- `docs/methodology.md`: evidence, prioritization, and pilot-design method.
- `docs/limitations.md`: explicit boundaries and prohibited claims.
- `docs/evaluation-plan.md`: the validation roadmap.
- `docs/project-overview.md` and `docs/Earnings_AI_Strategist_Project_Overview.pdf`: reader-facing project guide.
- `docs/portfolio-story-bank.md`: positioning, interview stories, demo script, and publication plan.
- `examples/pepsico/`: PepsiCo Q2 2026 public-data case study.
- `examples/jpmorgan-chase/`: JPMorgan Chase Q2 2026 public-data case study.

## Current status

Implemented and smoke-tested:

- Hermes specialist profile;
- custom domain skill;
- source hierarchy and evidence ledger;
- exact-quotation policy;
- transparent opportunity scoring;
- sensitivity warning;
- 30-day pilot contract;
- executive memo template.
- full public-data demonstrations for PepsiCo and JPMorgan Chase;
- public video demonstration;
- shareable project-overview PDF.

Not yet completed:

- practitioner review and a human-reviewed benchmark set;
- a dedicated SEC ingestion service;
- licensed transcript coverage;
- a standalone web application;
- measured recommendation accuracy, adoption, ROI, or time savings.

## Design principles

- Start with a recurring business decision, not a technology.
- Prefer first-party investor-relations and SEC sources.
- Treat management statements as claims, not independent verification.
- Keep fact, inference, and assumption separate.
- Tie every AI opportunity to a user, workflow, decision, data requirement, and non-AI baseline.
- Keep a human at the approval point.
- Use a shadow pilot before any high-impact automation.
- Treat missing evidence as an output rather than filling gaps with plausible text.

## Roadmap

1. Publish three reviewed company case studies across consumer goods, media, and financial services.
2. Add source-freshness and fiscal-period consistency checks.
3. Add exact-substring tests for quotations.
4. Export a structured evidence ledger.
5. Add editable scoring weights and sensitivity visualization.
6. Build a human-reviewed evaluation set.
7. Test a five-screen standalone interface.

## Disclaimer

This project is an independent demonstration using public information. It is not affiliated with or endorsed by companies analyzed by the agent. It does not provide investment, legal, accounting, or financial advice.

## License

MIT. See [LICENSE](LICENSE).
