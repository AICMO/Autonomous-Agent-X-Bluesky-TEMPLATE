# Learning: Template Initialization (Session 1)
Date: 2026-08-23
Status: Documented

## Context
This is a fresh clone of the Autonomous-Agent-X-Bluesky-TEMPLATE. No owner data has been configured yet. ME.md, GOALS.md, and platform credentials are all placeholder templates.

## What Was Found
- All required directories exist (agent/memory/, agent/outputs/, agent/state/, etc.)
- All skills are present (.claude/skills/publishing/, commenting/, discovery/, integrations/)
- Platform integrations are stubbed (agent/integrations/x/plan.md and bluesky/plan.md are templates)
- No content pillars defined (agent/memory/pillars.md is a template)
- No session state existed (created this session)

## Required Owner Actions (Before Agent Can Operate)
1. **Fill in ME.md** — Name, expertise areas, GitHub profile URL, current projects, links
2. **Fill in GOALS.md** — Target metric (followers, stars, etc.), deadline, constraints
3. **Configure X credentials** — Set GitHub Secrets: `X_API_KEY`, `X_API_SECRET`, `X_ACCESS_TOKEN`, `X_ACCESS_SECRET`, `X_BEARER_TOKEN`
4. **Configure Bluesky credentials** — Set GitHub Secrets: `BLUESKY_HANDLE`, `BLUESKY_APP_PASSWORD`
5. **Configure GitHub token** — Set `ANTHROPIC_API_KEY` and `GITHUB_TOKEN` or `GH_PAT` for agent operations
6. **Update platform plans** — Fill in agent/integrations/x/plan.md and agent/integrations/bluesky/plan.md with real account data
7. **Delete example files** — Remove agent/outputs/x/post-20260823-001.txt and agent/outputs/bluesky/post-20260823-001.txt after setup

## What the Agent Will Do Once Configured
1. Read ME.md → discover owner expertise and links
2. Read GOALS.md → understand target metrics and constraints
3. Run discovery skill → scan GitHub profile for promotable repos and live outputs
4. Define content pillars in agent/memory/pillars.md
5. Research pillar-relevant news → filter for owner-specific angles
6. Create posts following the publishing skill rules (pillar filter, length requirements, anti-AI patterns)
7. Queue management → respect 15-file hard limit
8. Engagement → find and reply to relevant accounts (see commenting skill)

## Key Constraints to Remember
- Queue hard limit: 15 files per platform. Never exceed.
- X posts: min 500 chars for news/opinion/BIP/promo posts (Premium account)
- Bluesky: max 290 chars per post (write separately from X, never shrink X posts)
- Every post must connect to a pillar. If it doesn't, skip it.
- No politics (politicians, legislation, elections — hard ban)
- Anti-AI writing rules: no em dashes, no banned words, vary sentence length

## Pipeline Verification
The workflow `process-outputs.yml` watches `agent/outputs/x/` and `agent/outputs/bluesky/` for `.txt` files.
Once credentials are configured, posts will be auto-published and moved to `posted/` on the schedule defined in `agent-work-trigger.yml`.
