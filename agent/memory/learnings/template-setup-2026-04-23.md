# Learning: Template Initialization Session

Date: 2026-04-23
Status: Bootstrap

## Context

This is the first session of a fresh template. The agent cannot create real content until the owner configures:
- ME.md (identity, expertise, projects, links)
- GOALS.md (target metric, deadline, success criteria)
- API credentials (X, Bluesky, Claude)

## What the Agent Needs to Bootstrap

### Minimum viable config (to start posting):
1. **ME.md** — at minimum: name, expertise areas, one project to promote
2. **GOALS.md** — one concrete metric (e.g., "100 followers in 30 days")
3. **ANTHROPIC_API_KEY** — required for the agent to run
4. **X_API_KEY, X_API_SECRET, X_ACCESS_TOKEN, X_ACCESS_SECRET** — required for X posting
5. **BLUESKY_HANDLE, BLUESKY_APP_PASSWORD** — required for Bluesky posting

### What the agent bootstraps itself (after config):
- `agent/memory/pillars.md` — discovers from ME.md + GOALS.md
- `agent/state/current.md` — created each session
- `agent/integrations/*/plan.md` — updates from API responses
- Content files — auto-created each session

## Template Example Source

See live agent for reference configuration:
- Live repo: https://github.com/AICMO/Autonomous-Agent-X-Bluesky
- ME.md example: see live repo
- GOALS.md example: see live repo

## First Real Session Checklist

Once owner fills in config:
1. Read ME.md — extract expertise areas → update pillars.md
2. Read GOALS.md — set goal metrics in state file
3. Check queue sizes (both should be 0 at start)
4. Do web research on pillar-relevant news
5. Create 2 content pieces (1 X, 1 Bluesky)
6. Create PR
