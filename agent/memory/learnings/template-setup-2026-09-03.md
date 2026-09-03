# Template Setup Guide
Date: 2026-09-03
Status: ACTIVE — awaiting owner configuration

## What This Repo Is
This is the Autonomous-Agent-X-Bluesky-TEMPLATE — a self-operating social media agent that:
- Runs on GitHub Actions (no server needed)
- Creates and posts content to X (Twitter) and Bluesky autonomously
- Reviews its own PRs and iterates based on what works
- Tracks metrics and adapts strategy over time

## Required Setup Steps (Owner Action Required)

### Step 1: Configure ME.md
Replace ALL `[placeholder]` values in `ME.md` with real information:
- Your name, location, background
- Current role and company
- Expertise areas (these become content pillars)
- GitHub profile URL (agent scans this to find promotable repos)
- LinkedIn, X, Bluesky profile links
- Content angles that reflect your real perspective

### Step 2: Configure GOALS.md
Replace ALL `[placeholder]` values with real targets:
- Primary metric (e.g., "X Followers: 1,000")
- Target number and deadline
- Start date (today)
- Constraints specific to your situation

### Step 3: Add Platform Credentials (GitHub Secrets)
Go to repo Settings → Secrets and variables → Actions:

**For X (Twitter):**
- `X_API_KEY` — from developer.twitter.com
- `X_API_SECRET`
- `X_ACCESS_TOKEN`
- `X_ACCESS_TOKEN_SECRET`

**For Bluesky:**
- `BLUESKY_HANDLE` — e.g., yourhandle.bsky.social
- `BLUESKY_APP_PASSWORD` — from Settings → App Passwords

### Step 4: Review agent/memory/pillars.md
Update with 3-5 content pillars aligned with your ME.md expertise areas.
The agent can also auto-discover these from ME.md if you leave them as placeholders.

### Step 5: Trigger first real work session
After the above steps, the agent will:
1. Read your ME.md and discover real pillars
2. Research news relevant to your pillars
3. Create content files in `agent/outputs/x/` and `agent/outputs/bluesky/`
4. Post them via the configured platform integrations

## What the Agent Figured Out This Session
- All configuration files contain placeholder values only
- Queues are empty (0 pending posts on both platforms)
- No platform credentials appear to be configured (X metrics not available)
- Agent cannot create pillar-filtered content without owner identity

## Key Constraint
The agent will NOT create generic filler content just to fill the queue.
Every post must connect to at least one pillar. Without ME.md configured,
there are no pillars, so there can be no content. This is by design.

## Expected First Real Session Output
Once configured, the first real agent session will:
- Discover 3-5 content pillars from ME.md
- Research 5-10 pillar-relevant news items
- Create 2 X posts + 2 Bluesky posts (queue starts empty, so max 2 each)
- Create a reply to an active account in the space
- Update pillars.md with discovered pillars
