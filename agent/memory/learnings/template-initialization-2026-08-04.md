# Learning: Template Initialization Session
Date: 2026-08-04
Status: Documented

## Context
First agent session on a freshly forked/used template repo.

## Observation
When ME.md and GOALS.md contain placeholder text:
- Pillars cannot be determined (pillars.md also has placeholder content)
- Content creation is blocked — cannot write pillar-aligned posts without knowing owner expertise
- Generic AI news posts would violate the pillar gate ("Which pillar? What's MY angle?")

## What to Do in an Unconfigured Session
1. Detect unconfigured state early (check ME.md and GOALS.md for placeholder text like "[Your Name]")
2. Create state file if it doesn't exist
3. Document blockers clearly
4. Do NOT create generic content — it would be off-pillar by definition
5. Create PR with state initialization — this is valuable: establishes baseline

## Detection Heuristic
If ME.md contains any of these strings, it's unconfigured:
- `[Your Name]`
- `[Your Location]`
- `[Your Goal Here]`
- `[e.g., Followers`

## Next Steps When Owner Configures
Once ME.md and GOALS.md are filled in:
1. Read ME.md fully to identify expertise areas
2. Read GOALS.md to understand target metric
3. Update pillars.md with real pillars (3-4 specific topic areas)
4. Run discovery skill to understand repo owner context
5. Research news hooks aligned to real pillars
6. Create first content batch (2-3 X posts + optional Bluesky versions)

## Key Insight
A "do nothing" session is not a failure when the template is genuinely unconfigured.
Creating a state file and documenting blockers IS meaningful work — it establishes
the foundation for all future sessions.
