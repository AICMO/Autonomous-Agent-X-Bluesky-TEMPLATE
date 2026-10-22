# Setup Checklist — Template Configuration
Date: 2026-10-22
Status: ACTIVE (not yet complete)

## Context
This is a fresh template repository. The agent ran its first session and found all configuration files contain placeholder values. This document records what needs to be done before the agent can operate autonomously.

## Checklist

### Phase 1: Identity & Goals (Owner Must Do)
- [ ] **ME.md** — Replace ALL `[placeholders]` with real data:
  - Name, location, background
  - Current role and company
  - Expertise areas (at least 3)
  - Current projects
  - GitHub profile URL (critical for OS scan)
  - LinkedIn, X, Bluesky profile links
  - Content angles for the agent

- [ ] **GOALS.md** — Define actual goal:
  - Target metric (e.g., "500 X followers")
  - Target number
  - Deadline
  - Start date
  - Constraints

### Phase 2: Platform Credentials (Owner Must Configure in GitHub)

**For X:**
- `X_API_KEY`
- `X_API_KEY_SECRET`
- `X_ACCESS_TOKEN`
- `X_ACCESS_TOKEN_SECRET`
- `X_BEARER_TOKEN`

**For Bluesky:**
- `BLUESKY_HANDLE`
- `BLUESKY_APP_PASSWORD`

See README.md for exact secret names and how to add them.

### Phase 3: Agent Configuration (Agent Does After Phase 1)
- [ ] **agent/memory/pillars.md** — Discover from ME.md, replace placeholders with real pillars
- [ ] **agent/integrations/x/plan.md** — Fill in account status, handle, follower count
- [ ] **agent/integrations/bluesky/plan.md** — Fill in account status, handle

### Phase 4: First Content Session (Agent Does After Phase 1+2)
- [ ] Research current news relevant to owner's pillars
- [ ] Create first batch of X content files (5-8 posts)
- [ ] Create first batch of Bluesky content files

## Notes
- The agent cannot create meaningful content without ME.md — all pillars, voice, and angles come from there
- The agent cannot post without credentials configured
- Once ME.md is filled in, the agent can immediately begin Phases 3+4
