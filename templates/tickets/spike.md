# Spike — Jira ticket template

```
Title: Spike — [Question this spike answers]
Type: Spike
Priority: Medium
Epic: [epic key, if applicable]

Description:
## Summary
[Plain-language description of what needs investigation — what and why]

## Specs
[Technical notes, scope, constraints — e.g., time budget, sample size]

## Questions
[Numbered list of questions the spike should answer]

## Current Flow
[As-is state]

## Proposed Flow
[To-be state — what we expect to validate or refute]

## Note
[Time budget, output expectations — typically a data packet, not a decision]

## Resources
[Links, docs, references — remove if none]

Labels: stream:[prospect|support|dev]
```

## Notes

- Spikes are time-boxed. Always include a time budget in Specs.
- Spikes return data and a recommendation, never a unilateral decision.
- If a spike reveals significant scope, follow up with a Story or Task — don't extend the spike.
