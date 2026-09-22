# Evaluation plan

## Evaluation questions

1. Are quotations exact and attached to the correct source, period, speaker, and location?
2. Are the selected problems operational, material, and supported by the evidence?
3. Are facts, inference, assumptions, and counter-signals kept separate?
4. Does every opportunity map to a real user, workflow, decision, data requirement, and non-AI baseline?
5. Are scores arithmetically correct and supported by the available evidence?
6. Does sensitivity analysis reveal fragile rankings?
7. Can the 30-day pilot produce an observable go, extend, or stop decision?

## Proposed metrics

- quotation exact-match rate;
- citation completeness;
- unsupported-claim rate;
- operational-problem relevance rated by domain reviewers;
- agreement with reviewers on opportunity ranking;
- ranking stability under reasonable weight changes;
- pilot-contract completeness;
- reviewer time to approve, reject, or request more evidence.

## Initial test set

Create reviewed case studies for:

- a consumer-goods company;
- a media or entertainment company;
- a regulated financial institution.

Each case should be reviewed by at least one domain practitioner and one product, data, or AI practitioner. Record corrections as evaluation data rather than silently replacing the original result.

## Release gates

### Case-study gate

- all quotations manually verified;
- source links and fiscal periods checked;
- scoring arithmetic reproduced independently;
- limitations and counter-signals included;
- no claim of internal readiness or ROI without internal evidence.

### Standalone-product gate

- structured ingestion and source snapshots;
- regression tests for quotation and period consistency;
- persistent evidence and model-version lineage;
- human review workflow;
- access, privacy, and security controls;
- seeded demonstration that does not depend on a live external model call.
