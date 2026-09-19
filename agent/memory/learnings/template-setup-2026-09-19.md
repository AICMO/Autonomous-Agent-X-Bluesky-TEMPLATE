# Learning: Template Setup Process
Date: 2026-09-19
Session: S1 (first session on unconfigured template)

## Context

This repository is a template. On first run, all configuration files contain placeholders, not real data. The agent detected this and documented the required setup steps instead of attempting to create meaningless content.

## Required Setup Steps (for repo owner)

### 1. Configure ME.md
Replace all `[placeholders]` with real information:
- Name, location, background
- Current role and company
- Expertise areas (these become content pillars)
- GitHub, X, LinkedIn, Bluesky profile URLs
- Current projects
- Content angles

### 2. Configure GOALS.md
Replace all `[placeholders]` with real objectives:
- Target metric (e.g., "500 X followers")
- Deadline
- Start date
- Success criteria

### 3. Configure agent/memory/pillars.md
Based on ME.md expertise, define 3-4 content pillars:
- What is the account's authoritative territory?
- What communities should be targeted?

### 4. Add Platform Credentials to GitHub
For X (Twitter):
- `X_API_KEY` — from developer.twitter.com
- `X_API_SECRET` — from developer.twitter.com
- `X_ACCESS_TOKEN` — from developer.twitter.com
- `X_ACCESS_TOKEN_SECRET` — from developer.twitter.com

For Bluesky:
- `BLUESKY_HANDLE` — your @handle
- `BLUESKY_PASSWORD` — your app password (not login password)

Add as GitHub repository secrets AND variables as needed.

### 5. Configure Platform Plan Files
Update `agent/integrations/x/plan.md` and `agent/integrations/bluesky/plan.md` with:
- Account status (free vs Premium)
- Handle
- Current follower count

## What Happens After Setup

Once configured, the agent will:
1. Read ME.md to discover content pillars
2. Research relevant news and topics
3. Create content files in `agent/outputs/{platform}/`
4. Workflows auto-post from those directories
5. Agent tracks engagement and improves over time

## Key Insight

The template is designed to be self-documenting. If a repo owner hasn't configured it, the agent should:
1. Document what's missing (not crash or produce garbage output)
2. Create example content to show the output format
3. Set up the state file for future sessions
4. Create a PR so the work is committed

This is the correct first-session behavior for an unconfigured template.
