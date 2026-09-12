# Template Setup Required
Date: 2026-09-12
Status: ACTIVE BLOCKER

## Summary

This repository is a fresh clone of the Autonomous-Agent-X-Bluesky-TEMPLATE. All key configuration files contain placeholder values. The agent cannot create meaningful content until the owner configures the following files.

## Required Configuration (in order)

### 1. ME.md (highest priority)
Fill in:
- Your name, location, background
- Current role and company
- Expertise areas (these become content pillars)
- Current projects
- All links (LinkedIn, GitHub, X, Bluesky)
- Content angles — what perspectives you bring

### 2. GOALS.md
Fill in:
- Your primary goal (e.g., "Reach 1000 X followers")
- Target metric and number
- Deadline
- Success criteria

### 3. agent/integrations/x/plan.md
Fill in:
- Your X handle
- Premium status (Active/Inactive)
- Current follower count
- Posting workflow configuration

### 4. agent/integrations/bluesky/plan.md
Fill in:
- Your Bluesky handle
- Posting workflow configuration

### 5. agent/memory/pillars.md
Derive from ME.md expertise areas. Example format:
```markdown
| **Autonomous Agents** — building and running AI agents in production | ME.md (owner expertise) |
| **AI infrastructure** — scaling AI systems for real workloads | ME.md (owner expertise) |
```

### 6. GitHub Secrets/Variables
Required for posting to work:
- X API credentials (see agent/integrations/x/requirements.txt)
- Bluesky credentials (see agent/integrations/bluesky/README.md)
- Check README.md for all required settings

## What the Agent Can Do After Setup

Once configured, the agent will:
1. Research news in your expertise areas
2. Create 2 content pieces per session (X + optional Bluesky)
3. Draft replies to relevant accounts in your space
4. Track metrics and adapt strategy

## What the Agent CANNOT Do

- Create content without pillars (no expertise direction = generic posts)
- Post without credentials configured
- Grow an audience without knowing the owner's identity/goals
