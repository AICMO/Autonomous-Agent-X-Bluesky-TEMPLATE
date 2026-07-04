# Setup Notes — 2026-07-04

## Status
This is a fresh template repository. No owner configuration exists yet.

## What Needs to Be Done (Owner Action Required)

### 1. Fill in ME.md
The agent uses ME.md every session to understand:
- Who the owner is
- What their expertise pillars are
- What links to promote
- What voice/angle to use

Without this, the agent has no basis for creating relevant content.

### 2. Fill in GOALS.md
The agent tracks progress toward a goal every session:
- What metric to grow (followers, stars, subscribers)
- What the target is
- What the deadline is

Without this, the agent has no direction.

### 3. Configure GitHub Secrets
The agent posts via API. Required secrets:
- `X_API_KEY`, `X_API_SECRET`, `X_ACCESS_TOKEN`, `X_ACCESS_SECRET` (X/Twitter API)
- `BLUESKY_HANDLE`, `BLUESKY_PASSWORD` (Bluesky)
- `ANTHROPIC_API_KEY` (Claude — the agent's brain)

### 4. Update pillars.md
Based on ME.md, define 3-5 content pillars:
- Topics where the owner has real authority
- Specific enough to filter noise, broad enough to post daily
- Connected to the account's goals

### 5. Update Integration Plan Files
- `agent/integrations/x/plan.md` — Account status, posting limits, Premium tier
- `agent/integrations/bluesky/plan.md` — Account status, posting limits

## What Exists (No Action Needed)
- Workflow infrastructure (GitHub Actions)
- Agent session protocol (CLAUDE.md)
- Publishing skill (`.claude/skills/publishing/SKILL.md`)
- Queue management system
- PR auto-merge pipeline

## First Real Session (After Setup)
Once configured, the first session should:
1. Read ME.md and GOALS.md → discover pillars
2. Check queue status
3. Research 1-2 pillar-relevant news stories
4. Create 2 content pieces (1 X post + 1 Bluesky version)
5. Create state file update with real metrics
