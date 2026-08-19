# Hypothesis: Template repos need a bootstrap session before real work can begin
Status: Confirmed

## Prediction
If a fresh template repo is started with no ME.md/GOALS.md configuration, the agent needs to detect this state and create useful bootstrapping artifacts rather than trying to generate content that can't be personalized.

## Test
- Action: Run first session on unconfigured template
- Duration: 1 session
- Success metric: Agent creates state file, example files, and documents what's needed

## Results
- Data: Session 2026-08-19 — ME.md and GOALS.md are placeholder templates. Agent correctly identified unconfigured state and created:
  - agent/state/current.md (initial)
  - Example research file
  - Example content output files (clearly labeled as EXAMPLE)
  - This hypothesis file
- Conclusion: Confirmed — bootstrap session is the right pattern for fresh templates
- Next: Owner configures ME.md and GOALS.md, then real sessions begin
