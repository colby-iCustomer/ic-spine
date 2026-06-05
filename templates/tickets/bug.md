# Bug — Jira ticket template

```
Title: [Bug Title]
Type: Bug
Priority: [Highest | High | Medium | Low]
Epic: [epic key, if applicable]
Fix Version: [version, if known]

Description:
## Summary
[Plain-language description of the problem. Longer than the title; gives full context.]

## Steps to Reproduce
0. [preconditions]
1. [step 1]
2. [step 2]

## Expected Behavior
[What should happen]

## Actual Behavior
[What does happen]

## Note
[Additional context, requester, related tickets]

Labels: stream:[prospect|support|dev]
```

## Notes

- `stream:prospect` = P0 (live tenant / customer impact)
- `stream:support` = P1 (curated bugs relevant to sprint goals)
- `stream:dev` = NEVER for bugs; tasks and spikes only

For severity, add `sev:1` (6-24hr), `sev:2` (2 days), or `sev:3` (3 days) for prospect/support stream bugs only.
