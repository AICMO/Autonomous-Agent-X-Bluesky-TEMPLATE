# Learning: Template Setup State Detection
Date: 2026-07-03
Session: S1 (first session)

## Observation

This repository is in template state. Both ME.md and GOALS.md contain placeholder text only. The agent detected this on first run.

## What the Agent Found

- `ME.md`: All fields are `[placeholders]` — no real identity, expertise, or links
- `GOALS.md`: All fields are `[placeholders]` — no real goal metric or deadline
- `agent/state/current.md`: Did not exist — created this session
- `agent/memory/pillars.md`: Template structure only, no real pillars defined
- Content queues: Empty (0 files in agent/outputs/x/ and agent/outputs/bluesky/)
- Platform integrations: Code exists but credentials not configured

## Key Insight

The agent cannot create relevant, personalized content until:
1. The owner's identity and expertise are defined in ME.md
2. The growth goal is defined in GOALS.md
3. Optionally: platform credentials are configured for auto-posting

## What This Agent Did

Instead of creating generic/placeholder content (which would be wasteful), this session:
1. Created `agent/state/current.md` to establish baseline state tracking
2. Created this learning doc to document the template detection pattern
3. Will create a PR to commit this foundation work

## Recommendation for Future Sessions

When the owner completes setup:
1. **First session post-setup**: Read ME.md → discover pillars → create/update pillars.md
2. **Then**: Research news/trends aligned with expertise pillars
3. **Then**: Create first content batch (5-8 pieces) per the publishing skill guidelines
4. **Queue check**: Always verify agent/outputs/x/ count before creating content

## Template Detection Heuristic

The agent can detect template state by checking:
```
grep -l "\[Your" ME.md GOALS.md
```
If these files contain `[Your` placeholder patterns, the repo is in template state.

## Priority Order When Owner Completes Setup

1. Read ME.md fully — extract: name, expertise, current projects, links, content angles
2. Read GOALS.md — extract: metric, target number, deadline, constraints
3. Update pillars.md with real pillars from ME.md + GOALS.md
4. Research 3-5 recent news items per pillar
5. Create first content batch

This is the correct agent startup sequence for a newly configured repo.
