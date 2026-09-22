# Earnings → AI Strategist: portfolio story bank

## 1. The honest headline

I built a specialized Hermes agent that turns a public company's latest earnings materials into an evidence-backed AI strategy memo. It identifies three operational problems, ties each one to exact source quotations, ranks possible AI interventions using a visible scoring model, and proposes one bounded 30-day pilot for executive approval.

The current version is a working specialist bot and reusable analysis workflow. It is not yet a standalone SaaS product, an automated SEC data pipeline, or a proven production system. I have configured and smoke-tested the agent, its research rules, scoring logic, pilot framework, and document template. The next proof point is to run complete company case studies and test the quality of its recommendations with practitioners.

## 2. One-line descriptions for different audiences

### General audience

I built a bot that reads a company's latest earnings documents and turns them into a practical AI pilot recommendation, with citations showing where every important claim came from.

### Recruiter

I designed a specialist AI strategy agent that converts earnings calls, SEC filings, and investor presentations into an auditable executive memo: three operational problems, ranked AI opportunities, and one measurable 30-day pilot.

### Consulting leader

The tool compresses the first phase of AI opportunity discovery. It moves from public evidence to a decision-ready hypothesis, while keeping management claims, analyst inference, and unverified assumptions separate.

### Technical interviewer

I implemented a Hermes profile with a custom system persona, a domain-specific skill, an evidence ledger, deterministic multi-criteria scoring, human approval gates, and document-generation requirements. The system uses web research and document extraction for evidence, code for calculations, and PDF/DOCX tools for the final memo.

### Executive

Give it a public company. It will show you which operating problems are visible in the latest disclosures, which AI use cases appear defensible, what evidence is still missing, and what a low-risk 30-day pilot could look like.

## 3. Thirty-second pitch

Most AI idea lists start with the technology and work backward toward a business problem. I built the opposite. Earnings → AI Strategist starts with a company's own disclosures: the latest earnings release or remarks, SEC filing, and investor presentation. It extracts exact evidence, identifies three operational constraints, ranks possible interventions by impact, feasibility, data readiness, and risk, and produces one tightly scoped 30-day pilot. The output is an executive memo with citations, assumptions, guardrails, and a go, extend, or stop decision at the end of the pilot.

## 4. Two-minute origin story

I wanted to build something that showed strategy judgment, not another general-purpose chatbot. The first idea was a broad AI opportunity finder, but that shape had a problem: without evidence, it could produce recommendations that sounded plausible for almost any company.

I narrowed the product around a recurring executive decision: "Which operating problem deserves an AI pilot now?" Public-company earnings materials gave me a repeatable evidence base. They are imperfect, because they describe the business from management's perspective and omit internal workflow data, but they are timely, attributable, and available across sectors.

From there, I designed an evidence-to-decision workflow. The agent first establishes the company, fiscal period, and as-of date. It then builds a source manifest and checks exact quotations before selecting three operational problems. It keeps facts separate from interpretation and assumptions. Only after that does it generate AI opportunities.

The opportunities are scored with a visible formula rather than a vague model judgment. The top defensible option becomes a 30-day shadow pilot with a baseline, target, owner role, human review points, guardrails, and a stop condition. The tool ends with an approval package rather than an open-ended chat response.

The result is a working specialist agent inside Hermes, supported by a custom skill and memo template. I have verified that the profile loads, the skill is enabled, the bot is recognized in Bot Mode, authentication works, and the core behavior passes a live smoke test. Full company case studies and user validation are the next stage.

## 5. The problem I chose

AI strategy teams often face three related problems:

- Company disclosures contain useful operating signals, but the evidence is spread across transcripts, filings, and presentations.
- Generic AI ideation produces long lists of use cases without enough connection to a real workflow, decision owner, or dataset.
- Recommendations often hide uncertainty. Projected value, inferred readiness, and management claims can get presented as if they were established facts.

The product addresses the front end of AI strategy work: creating a defensible opportunity hypothesis and a small validation plan. It does not replace internal discovery, security review, process mapping, technical architecture, or financial approval.

## 6. What I actually created

### A specialist Hermes bot

Profile name: `earnings-strategist`  
Display name: `Earnings → AI Strategist`

The bot has a dedicated role, persistent profile, model configuration, credentials, tools, memory boundary, and chat history. Its standing instructions define the research workflow, evidence standards, opportunity scoring, pilot design, and final deliverables.

### A domain-specific skill

Skill name: `earnings-call-ai-strategy`

The skill contains the reusable operating method. It defines:

- the source hierarchy;
- the definition of done;
- the evidence-ledger schema;
- rules for selecting the three problems;
- the opportunity-scoring formula;
- the 30-day pilot contract;
- memo-production requirements.

This separation matters. The bot's persona defines how it should behave, while the skill defines how to perform this specific class of work consistently.

### An executive memo template

The template turns the analysis into an approval document with:

1. the decision requested;
2. an executive summary;
3. company and reporting-period scope;
4. a source manifest;
5. three operational problems with exact quotations;
6. ranked AI opportunities;
7. one recommended 30-day pilot;
8. risks, assumptions, and non-goals;
9. an executive approval checklist;
10. an evidence appendix.

### A transparent scoring model

Each opportunity receives a 1-to-5 score for:

- impact: 35%;
- feasibility: 25%;
- data readiness: 25%;
- risk-adjusted safety: 15%.

The formula is:

`0.35 × impact + 0.25 × feasibility + 0.25 × data readiness + 0.15 × (6 − risk)`

Risk is scored from 1 for low risk to 5 for high risk. The calculation is done in code, shown to the reader, and paired with a sensitivity warning. If a small change in assumptions changes the winner, the ranking is labeled fragile.

### A 30-day pilot framework

The selected opportunity becomes a four-stage pilot:

- Days 1–5: validate the workflow, data, baseline, and controls.
- Days 6–12: build a frozen-data prototype and non-AI baseline.
- Days 13–21: test errors, user acceptance, and red-team cases.
- Days 22–30: run a shadow pilot without autonomous high-impact action.

The day-30 decision is explicit: stop, extend, or proceed to a controlled production phase.

## 7. How the tool works

### User journey

1. The user enters an unambiguous public company name or ticker.
2. The bot identifies the latest completed reporting period and states the analysis date.
3. It collects the strongest available first-party materials.
4. It creates a source manifest before making recommendations.
5. It verifies exact quotations and builds an evidence ledger.
6. It selects exactly three operational problems.
7. It labels each statement as fact, inference, or assumption.
8. It generates bounded AI opportunities tied to named users and workflows.
9. It scores the opportunities with a visible formula.
10. It recommends one 30-day pilot and exports an executive memo.

### Inputs

Minimum input:

- company name or ticker.

Public research inputs:

- latest investor-relations earnings release;
- prepared remarks or official earnings transcript when available;
- SEC 10-Q or 10-K for the same reporting context;
- investor presentation;
- publication date, fiscal period, speaker or filing section, page or anchor, and URL.

Internal inputs needed before a real pilot can be approved:

- process owner and frontline user;
- workflow volume and baseline performance;
- system and data inventory;
- data quality and access constraints;
- privacy, security, legal, and model-risk requirements;
- implementation effort and operating cost;
- success threshold and stop condition.

The public-data analysis can identify hypotheses. It cannot establish internal data readiness, ROI, or implementation feasibility by itself.

### Outputs

- company, ticker, fiscal period, and as-of date;
- source manifest with working links;
- exactly three operational problems;
- exact quotations supporting each problem;
- fact, inference, and assumption labels;
- counter-signals and missing evidence;
- confidence rating for each problem;
- ranked AI opportunity table;
- component scores, formula, rationale, and sensitivity warning;
- one 30-day pilot plan;
- risks, guardrails, non-goals, and stop condition;
- executive approval checklist;
- PDF memo and editable DOCX when the document tools are available.

## 8. What it can do today, and what it cannot yet do

### Current capabilities

- Research a named public company using web and document tools.
- Prioritize first-party investor-relations and SEC sources.
- Distinguish the fiscal period from the publication date.
- Verify quotations against extracted text.
- Create a claim-level evidence ledger.
- Identify operational problems rather than generic market themes.
- Generate AI use cases tied to a workflow, user, decision, and required data.
- Score opportunities transparently.
- Flag fragile rankings and missing evidence.
- Design a human-reviewed 30-day pilot.
- Produce a structured executive memo.

### Current boundaries

- It is a Hermes specialist bot, not a standalone website or mobile app.
- It does not yet call a dedicated SEC EDGAR API through a custom ingestion service.
- It does not have licensed access to every earnings-call transcript.
- It has not yet been benchmarked on a human-reviewed set of company cases.
- It does not know a company's internal architecture, costs, ownership, or data quality unless the user supplies them.
- It does not prove ROI, causality, or production readiness from public data.
- It does not execute an AI pilot or take autonomous business actions.
- It is not investment advice or an equity-valuation tool.

This distinction is important when presenting the project. The strength of the current build is the decision workflow and evidence discipline. Production integrations and validation are the next layer.

## 9. Design ideas and frameworks behind the product

### Jobs to Be Done

The product is designed around a specific job:

"When I need to decide where a public company could test AI, I want to turn its latest operating disclosures into a short list of evidence-backed opportunities, so I can choose one pilot without pretending public data tells me everything."

This framing prevented the product from becoming a general research assistant.

### Evidence → problem → opportunity → pilot → approval

This is the central operating model. It forces the system to earn each recommendation through an earlier layer. A use case cannot appear unless it maps to a problem; a pilot cannot be recommended unless the use case has an evidence trail and an explicit score.

### Source hierarchy and provenance

The agent prefers official investor-relations materials and SEC filings, then uses secondary transcript providers only when a first-party source is missing. Every important claim retains its source, date, period, and location.

### Fact, inference, and assumption separation

A management quotation is a fact about what management said. It is not automatically proof that management's interpretation is correct. The bot keeps sourced observations, analyst interpretation, and missing internal information in separate fields.

### Multi-criteria decision analysis

The weighted score makes the recommendation inspectable. Executives can disagree with the weights or component scores, but they can see what drove the result. Sensitivity analysis prevents a fragile ranking from looking precise.

### Human-in-the-loop decision design

The tool recommends; a person approves. The pilot uses a shadow mode before any high-impact automation. The output includes review points, escalation paths, and stop conditions.

### Pilot-before-platform

The system recommends one bounded workflow and one 30-day experiment instead of a large transformation roadmap. This reduces cost and turns uncertainty into something measurable.

### Responsible-AI claim discipline

The tool does not present public evidence as internal truth. It avoids unsupported ROI, readiness, prevalence, and causality claims. Missing evidence is treated as an output, not an inconvenience to hide.

## 10. Integrations and technical architecture

### Current platform

- Hermes Agent Bot Mode for the persistent specialist profile.
- Custom `SOUL.md` for standing role and behavior.
- Custom skill for the domain workflow and definition of done.
- Hermes web search, extraction, and browser tools for research.
- File and document extraction for SEC filings, presentations, and transcripts.
- Code execution for deterministic scoring and checks.
- DOCX and PDF tooling for executive deliverables.
- Persistent profile state for repeated use and future learning.

### Logical architecture

`Company input`  
→ `source discovery`  
→ `source manifest`  
→ `document extraction`  
→ `quotation verification and evidence ledger`  
→ `three operational problems`  
→ `controlled AI opportunity generation`  
→ `deterministic scoring and sensitivity check`  
→ `30-day pilot design`  
→ `executive memo and approval checklist`

### Useful next integrations

- SEC EDGAR submissions and company-facts APIs for structured filing discovery.
- Investor-relations RSS feeds or company-specific monitoring.
- A licensed transcript provider for consistent transcript coverage.
- A small database for source snapshots, evidence records, model versions, and prior analyses.
- A lightweight web interface for company selection, evidence review, weight adjustment, and memo export.
- An evaluation harness with a human-reviewed gold set.
- GitHub Actions for linting the skill package, checking templates, and validating example outputs.

## 11. Trade-offs I made

### Evidence depth versus speed

Exact quotations and source manifests slow the workflow, but they reduce the risk of a polished memo resting on invented or misattributed evidence. I chose defensibility over instant output.

### Three problems versus exhaustive analysis

Restricting the memo to three problems makes it usable for an executive. It can exclude legitimate secondary issues, so the system should retain an appendix or backlog for future review.

### Transparent scoring versus apparent intelligence

A visible weighted formula is less sophisticated than an opaque model ranking. It is easier to challenge, reproduce, and revise. I chose inspectability over the appearance of precision.

### Public evidence versus internal truth

Public disclosures make the product repeatable and easy to demonstrate. They omit internal costs, workflow detail, system constraints, and data quality. I treat the output as a strategy hypothesis, not a final investment case.

### One pilot versus a transformation roadmap

One 30-day pilot may feel narrow to stakeholders who want a large AI roadmap. The narrow scope creates a measurable learning loop and reduces the cost of being wrong.

### Human approval versus full automation

The bot could be designed to make the decision automatically. I kept approval with a human and required shadow testing because the evidence is incomplete and the business consequences can be material.

### Strict source hierarchy versus broad coverage

First-party materials are attributable but can be selective and promotional. Secondary research may add useful context but introduces licensing and provenance issues. The current design uses first-party evidence as the core and requires counter-signals rather than treating management statements as neutral truth.

### Hermes profile versus standalone product

Building inside Hermes made the specialist agent fast to create, tool-rich, persistent, and easy to extend. The trade-off is distribution: a general user needs Hermes to install the complete profile unless I build a standalone interface later.

### Fixed weights versus company-specific priorities

The weights create a consistent starting point. A bank, media company, and consumer-goods company may reasonably weight risk, feasibility, and impact differently. The next interface should let users change weights and immediately see whether the recommendation changes.

## 12. Story bank for interviews and networking

### Story 1: Why I built it

**Prompt:** Tell me about an AI product you designed.

**Answer:** I wanted a project that demonstrated how I make AI investment decisions, not just how I prompt a model. I focused on the recurring question of which operating problem deserves an AI pilot. I used earnings materials because they provide current, attributable evidence across industries. I then designed a workflow that moves from exact evidence to three problems, ranks bounded interventions, and ends with one 30-day pilot. The project shows my approach to strategy: narrow the decision, make assumptions visible, and define how the recommendation will be tested.

### Story 2: How I avoided building a generic chatbot

**Prompt:** How did you differentiate the product?

**Answer:** The early version could have been a chat interface over annual reports. I rejected that because retrieval alone does not produce a decision. I made the output contract much stricter: exactly three operational problems, exact quotations, a controlled opportunity table, transparent scoring, and one approval-ready pilot. The bot is useful because of the workflow and guardrails, not because it has a chat box.

### Story 3: A difficult trade-off

**Prompt:** What trade-off did you make?

**Answer:** I chose public evidence even though it cannot establish internal readiness. That made the product demonstrable and repeatable, but it created a risk of overclaiming. I handled that by separating fact, inference, and assumption, lowering confidence when sources are incomplete, and making internal validation a required part of the pilot. The tool produces a defendable hypothesis, not a pretend business case.

### Story 4: Responsible AI

**Prompt:** How did you account for AI risk?

**Answer:** I treated evidence quality as part of the product architecture. Quotations must match the source. Management claims are labeled as claims. The ranking penalizes risk, and fragile rankings are flagged. The recommended pilot runs in shadow mode and keeps a person at the approval point. It also has an explicit stop condition. Responsible AI here is not a separate checklist at the end; it shapes what the system is allowed to claim and do.

### Story 5: Turning ambiguity into a pilot

**Prompt:** How do you approach an unclear business problem?

**Answer:** I start by naming the recurring decision and the person who owns it. In this tool, the decision is which operating problem deserves an AI pilot. I then ask what evidence would support that decision, what the public sources cannot tell us, and what we can test in 30 days. That turns a broad request for an "AI strategy" into one workflow, one baseline, one target, and one go-or-stop decision.

### Story 6: Bridging business and technical teams

**Prompt:** How do you communicate between executives and technical teams?

**Answer:** I use linked artifacts. The executive sees the problem, evidence, ranking, risk, and decision requested. The delivery team sees the required data, baseline, review queue, evaluation plan, guardrails, and stop condition. Both views come from the same evidence ledger and pilot contract, so the strategy does not disappear when implementation starts.

### Story 7: What is not finished

**Prompt:** What would you improve next?

**Answer:** The workflow is implemented and smoke-tested, but it still needs complete case studies and human evaluation. I would run it on companies from three sectors, have domain practitioners score evidence quality and recommendation usefulness, and build a regression set for quotation accuracy and scoring consistency. After that, I would add structured SEC ingestion and a small interface for reviewing evidence and changing weights.

### Story 8: What I learned

**Prompt:** What did the project teach you?

**Answer:** The hardest part of an AI strategy tool is not generating ideas. It is controlling the chain between evidence and action. Once I forced every use case to point to a source-backed problem, an owner, a workflow, a dataset, and a measurement plan, many attractive ideas stopped surviving. That was useful. A smaller set of defensible options is more valuable than a long list of plausible ones.

## 13. How other people can use it

### Simple instruction

Open the `Earnings → AI Strategist` bot and enter:

> Analyze PepsiCo and produce the latest earnings-to-AI strategy memo.

### Better instruction for a targeted analysis

> Analyze The Walt Disney Company using its latest completed reporting period. Focus on operational problems in streaming, content operations, and customer service. Use first-party investor materials and the relevant SEC filing. Produce the cited memo, show the opportunity scores, and recommend one 30-day pilot. Treat any internal-data assumption as unverified.

### Reviewer instruction

> Review this memo as a skeptical COO. Check whether every problem is supported, whether quotations are exact, whether the opportunity is connected to a real workflow, and whether the 30-day pilot could produce a go-or-stop decision. Return required corrections before approval.

### Weight-change instruction

> Recalculate the ranking with risk-adjusted safety at 30%, impact at 30%, feasibility at 20%, and data readiness at 20%. Show whether the selected pilot changes and label the ranking fragile if reasonable weight changes reverse it.

## 14. How to showcase it

### Best portfolio package

Create three complete case studies:

1. PepsiCo for consumer goods and supply-chain or commercial operations.
2. Disney for media, streaming, content operations, or customer experience.
3. JPMorgan Chase for financial-services operations, compliance, service, or knowledge work.

For each case, publish:

- a one-page case-study page;
- the executive memo PDF;
- a redacted evidence ledger;
- the scoring table;
- a simple architecture diagram;
- a three-to-five-minute demo video;
- a short note on what public evidence could not prove.

Do not claim the company uses or endorsed the recommendation. State that the analysis is an independent demonstration using public information.

### Portfolio-page structure

1. Question: Which operating problem should this company test with AI?
2. Context: company, fiscal period, and source set.
3. Method: evidence ledger, problem selection, scoring, pilot design.
4. Findings: three problems and ranked opportunities.
5. Recommendation: one 30-day pilot.
6. Limitations: missing internal data and uncertain assumptions.
7. Artifact: downloadable memo and demo video.
8. Reflection: what changed after review.

### Three-minute demo script

**0:00–0:20**  
"Most AI strategy decks begin with a list of use cases. This tool starts with evidence."

**0:20–0:45**  
Enter a company and show the reporting-period scope and source manifest.

**0:45–1:20**  
Open one operational problem. Show the exact quotation, the source location, the inference, the counter-signal, and the missing internal evidence.

**1:20–1:50**  
Show the opportunity table and explain the visible scoring formula. Change one weight if the interface supports it, or explain the sensitivity result.

**1:50–2:35**  
Open the recommended 30-day pilot. Point to the user, baseline, target, human approval point, guardrail, and stop condition.

**2:35–3:00**  
Show the downloadable memo and close with the limitation: public disclosures can generate a hypothesis, but internal discovery determines whether the pilot should proceed.

### LinkedIn post draft

I built an AI strategy agent around a decision I keep seeing companies struggle with: which business problem actually deserves an AI pilot?

The input is simple: a public company.

The agent reads the latest earnings materials, 10-Q or 10-K, and investor presentation. It then produces:

- three operational problems supported by exact quotations;
- a clear separation between facts, interpretation, and assumptions;
- AI opportunities ranked by impact, feasibility, data readiness, and risk;
- one 30-day pilot with a baseline, target, human approval point, and stop condition;
- an executive memo with source links.

The important design choice was what the tool refuses to do. It does not treat public disclosures as internal truth. It does not invent ROI. It does not recommend a broad transformation roadmap. It creates a decision hypothesis that an executive team can challenge and validate.

I am now testing it across consumer goods, media, and financial services. The next step is to compare its recommendations with practitioner reviews and publish the case studies.

### Resume or portfolio bullets

Use one of these only after linking to a public case study:

- Built a specialist AI strategy agent that converts earnings calls, SEC filings, and investor presentations into cited executive memos, ranked use cases, and 30-day pilot plans.
- Designed an auditable evidence-to-decision workflow with exact-quote verification, fact/inference/assumption controls, weighted opportunity scoring, sensitivity flags, and human approval gates.
- Productized AI opportunity discovery into a repeatable framework spanning source provenance, operational problem selection, use-case prioritization, pilot design, and executive decision support.

Do not add adoption, time-saved, recommendation-accuracy, or ROI metrics until they have been measured.

## 15. Publishing it on GitHub

Yes. The safest and most useful GitHub version is a curated Hermes profile distribution or a public project repository containing the non-secret parts of the agent.

### What to publish

```text
earnings-ai-strategist/
├── README.md
├── SOUL.md
├── profile.yaml
├── skills/
│   └── ai-strategy/
│       └── earnings-call-ai-strategy/
│           ├── SKILL.md
│           └── references/
│               └── executive-memo-template.md
├── examples/
│   ├── pepsico/
│   │   ├── README.md
│   │   ├── source-manifest.csv
│   │   ├── evidence-ledger.csv
│   │   └── executive-memo.pdf
│   └── ...
├── docs/
│   ├── architecture.md
│   ├── methodology.md
│   ├── limitations.md
│   └── evaluation-plan.md
├── tests/
│   ├── quote-verification-cases.json
│   └── scoring-cases.json
├── .gitignore
├── LICENSE
└── CONTRIBUTING.md
```

### What not to publish

- `.env` files;
- API keys, OAuth tokens, cookies, or credential stores;
- `auth.json`;
- personal memories or `USER.md`;
- sessions, state databases, chat histories, or logs;
- private source documents or licensed transcript content;
- complete cloned profile archives without a manual privacy review;
- generated claims that have not been checked against their sources.

Hermes profile distributions are designed for sharing a complete agent while keeping each installer's memories, sessions, and API keys separate. Git itself will not automatically protect secrets, so create and verify `.gitignore` before the first commit and inspect `git status` carefully.

### Recommended repository positioning

Repository name: `earnings-ai-strategist`  
Description: `A Hermes specialist agent that turns public-company earnings materials into cited AI opportunity memos and 30-day pilot plans.`

Suggested topics:

`ai-strategy`, `decision-intelligence`, `sec-filings`, `earnings-calls`, `hermes-agent`, `responsible-ai`, `executive-memos`

### README opening

> Earnings → AI Strategist is a shareable Hermes agent for evidence-backed AI opportunity discovery. Given a public company, it analyzes the latest earnings materials, identifies three operational problems supported by exact quotations, ranks bounded AI interventions, and proposes one human-reviewed 30-day pilot. It is a strategy hypothesis generator, not investment advice or a substitute for internal discovery.

### GitHub release path

1. Curate a clean repository rather than pushing the live profile directory blindly.
2. Add `.gitignore` before `git add`.
3. Include one fully reviewed example.
4. Add a methodology and limitations page.
5. Add tests for quotation matching and scoring arithmetic.
6. Record a demo GIF or short video and link it from the README.
7. Tag the first stable package as `v0.1.0`.
8. Invite reviewers to challenge the evidence and pilot recommendation, not just the interface.

The machine is currently authenticated to GitHub as `vedantjainsc-hub`, so the repository can be created and pushed when the package and first case study are ready. No repository has been published as part of this story bank.

## 16. Suggested publication sequence

### Stage 1: prove one case

Run a complete analysis on one company. Manually review every quotation, score, assumption, and link. Ask one domain practitioner and one product or data practitioner to critique it.

### Stage 2: make it repeatable

Run two more sectors. Track where the workflow breaks: transcript availability, fiscal-period mismatch, weak evidence, scoring disagreement, or pilots that require unavailable data.

### Stage 3: publish the method

Release the clean GitHub repository, the methodology, one or more example memos, and an evaluation plan. Keep uncertain results labeled.

### Stage 4: publish the story

Create:

- one LinkedIn launch post;
- one three-minute product demo;
- one eight-to-twelve-minute YouTube case study;
- one portfolio project page;
- one downloadable sample memo.

### Stage 5: test demand

Offer five strategy professionals or operators a free analysis of a company they know. Ask them to rate:

- evidence accuracy;
- problem relevance;
- usefulness of the opportunity ranking;
- pilot realism;
- missing information;
- whether they would use the memo in an internal discussion.

Do not treat positive comments as proof of impact. Measure whether users can make a clearer decision and whether reviewers identify fewer unsupported claims over successive versions.

## 17. Next-step roadmap

### Immediate: build proof

1. Produce the first full company memo.
2. Verify every quotation against the original source.
3. Ask two reviewers to score the memo with a written rubric.
4. Revise the skill based on failure patterns.
5. Publish a redacted case study and demo.

### Product quality

- Add a source freshness check.
- Add automated exact-substring tests for quotations.
- Add fiscal-period consistency checks.
- Add a structured evidence-ledger export.
- Add weight editing and sensitivity visualization.
- Add a confidence rubric for problem selection.
- Add a non-AI baseline for every opportunity.

### Evaluation

Create a gold set of reviewed cases and measure:

- quotation accuracy;
- citation completeness;
- operational-problem relevance;
- unsupported-claim rate;
- agreement with human reviewers on opportunity ranking;
- pilot completeness;
- ranking stability under weight changes;
- time required for a reviewer to approve or reject the memo.

### Standalone product path

If practitioner demand is real, build a lightweight web application with five screens:

1. company and reporting-period selection;
2. source manifest and evidence review;
3. three operational problems;
4. ranked opportunities with editable weights;
5. pilot approval and memo export.

Keep the agent behind the workflow. Do not turn the product into an unrestricted chat interface.

### Commercial path

Potential offers:

- a public-company AI opportunity brief;
- a sector benchmark comparing recurring operational problems;
- a workshop that validates the public-data hypothesis against internal workflows;
- a 30-day pilot design sprint;
- a recurring quarterly strategy update.

The public memo can open the conversation. Paid work begins where confidential process, data, governance, and implementation details are required.

## 18. Questions I should be ready to answer

- Why use earnings materials instead of news or annual reports alone?
- How do you know the three selected problems are the most important?
- How do you verify that a quotation is exact?
- Why these scoring weights?
- What happens when the ranking is fragile?
- How do you prevent the bot from inventing ROI or internal capabilities?
- What would make you stop a pilot?
- How would the workflow change in a regulated industry?
- What part is deterministic and what part uses a language model?
- How would you evaluate recommendation quality?
- What user feedback have you collected?
- Why is this a bot rather than a dashboard?
- What would you need to make it production-ready?

## 19. The strongest way to position myself

This project supports a specific professional identity:

> I design AI decision workflows that connect messy evidence to a bounded business action. I focus on source quality, transparent prioritization, human approval, and measurable pilots rather than producing generic use-case lists.

The project demonstrates:

- business problem framing;
- AI opportunity discovery;
- executive communication;
- evidence and source governance;
- prioritization under uncertainty;
- responsible-AI controls;
- pilot design;
- product thinking;
- translation between business and technical teams;
- honest treatment of limitations.

The credibility of the story will come from the case studies and review evidence, not from calling the bot "production-ready." The most persuasive next artifact is one excellent, fully audited company memo.