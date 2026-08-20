# Setup Checklist — Template Configuration Required
Date: 2026-08-20
Status: PENDING OWNER ACTION

## Summary

This repository is an unconfigured template. The agent detected that all key identity and goal files contain placeholder content. The agent cannot create meaningful content until the owner completes the steps below.

## Required Configuration Steps

### Step 1: Fill in ME.md (Owner Identity)
File: `ME.md`

Replace all `[placeholder]` fields with real information:
- `Name` — your actual name
- `Location` — your city/region
- `Background` — your professional summary (e.g., "10+ years building AI products")
- `Current Role` — your title and company
- `Expertise Areas` — 3-5 specific areas you have authority in
- `Current Projects` — what you're building (this becomes content fuel)
- `GitHub`, `LinkedIn`, `X`, `Bluesky` — your actual profile URLs
- `Content Angles` — how you want to be perceived (founder, expert, builder, etc.)

### Step 2: Fill in GOALS.md (What to Achieve)
File: `GOALS.md`

Define:
- `Target Metric` — e.g., "1000 X followers" or "500 Bluesky followers"
- `Target Number` — specific number
- `Deadline` — timeframe (e.g., "90 days from 2026-08-20")
- `Start Date` — today: 2026-08-20
- `Constraints` — what the agent must NOT do (e.g., no paid promotion)
- `Success Criteria` — how you'll know you've succeeded

### Step 3: Update agent/memory/pillars.md (Content Pillars)
File: `agent/memory/pillars.md`

Define 3-5 content pillars based on your expertise from ME.md:
- Each pillar = a topic area you can post about with authority
- Pillars filter what news the agent will use as hooks
- Example: "AI product development," "Founder lessons," "Autonomous agents"

### Step 4: Configure Platform Credentials (via GitHub Secrets)

See README.md → Setup section for full instructions. Required secrets:
- **X (Twitter):** `X_CONSUMER_KEY`, `X_CONSUMER_SECRET`, `X_ACCESS_TOKEN`, `X_ACCESS_TOKEN_SECRET`
- **Bluesky:** `BLUESKY_HANDLE`, `BLUESKY_APP_PASSWORD`

Verify setup: `gh variable list` (variables indicate secrets are likely configured)

### Step 5: Update Integration Plan Files

After configuring credentials, update:
- `agent/integrations/x/plan.md` — fill in handle, follower count, posting limits
- `agent/integrations/bluesky/plan.md` — fill in handle, tier, posting limits

## What Happens After Setup

Once configured, the agent will:
1. Research current news through your expertise pillars
2. Draft X posts (500-1000 chars for news/opinion)
3. Draft Bluesky posts (under 290 chars, written separately)
4. Queue posts in `agent/outputs/x/` and `agent/outputs/bluesky/`
5. Workflows auto-post to each platform
6. Agent tracks metrics and adjusts strategy

## Why This Matters

Without owner identity (ME.md), the agent cannot:
- Pass the pillar gate (which pillar does this connect to? what's MY angle?)
- Write in the owner's voice
- Promote relevant repos or live outputs
- Target relevant communities

Generic content from an unconfigured agent will underperform. The 15-30 minutes to fill in ME.md and GOALS.md has outsized impact on every future session.
