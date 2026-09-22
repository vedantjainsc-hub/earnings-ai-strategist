# Methodology

## Decision being supported

Every reporting cycle, a strategy or operating leader decides which bounded business workflow deserves an AI pilot, using current operating evidence while balancing impact, feasibility, data readiness, and risk.

## Evidence sequence

1. Resolve the company, ticker, completed fiscal period, and analysis date.
2. Collect first-party earnings materials, the relevant SEC filing, and the investor presentation.
3. Build a source manifest before drawing conclusions.
4. Verify exact quotations against extracted source text.
5. Select exactly three operational problems.
6. Separate facts, interpretation, assumptions, counter-signals, and missing evidence.
7. Generate AI opportunities tied to a named user, workflow, decision, data requirement, and non-AI baseline.
8. Score the opportunities using the documented formula.
9. Test whether reasonable changes to assumptions or weights reverse the winner.
10. Convert the highest-ranked defensible opportunity into a 30-day shadow pilot.

## Source hierarchy

1. Company investor-relations earnings release, prepared remarks, and official transcript.
2. SEC 10-Q or 10-K for the same reporting context.
3. Company investor presentation.
4. Secondary transcript provider only when a first-party transcript is unavailable.

Search snippets are discovery aids and do not count as evidence.

## Evidence contract

Every consequential claim should preserve:

- a stable claim identifier;
- the linked operational problem;
- an exact quotation;
- speaker or filing section;
- source title and type;
- fiscal period and publication date;
- page, heading, or transcript anchor;
- direct URL;
- analyst interpretation;
- limitation or counter-signal.

## Opportunity scoring

`weighted_score = 0.35*impact + 0.25*feasibility + 0.25*data_readiness + 0.15*(6-risk)`

Each input uses a 1-to-5 scale. The system shows component scores and reasons. Unsupported internal readiness should not receive a high score. If small reasonable changes alter the winner, the ranking is fragile and requires more evidence.

## Pilot contract

- Days 1–5: validate the workflow, data, baseline, and controls.
- Days 6–12: build a frozen-data prototype and non-AI baseline.
- Days 13–21: test errors, user acceptance, and red-team cases.
- Days 22–30: run a shadow pilot without autonomous high-impact action.

The day-30 decision is stop, extend, or proceed to a controlled production phase.
