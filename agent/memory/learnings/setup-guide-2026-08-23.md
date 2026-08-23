# Setup Guide: Initializing the Autonomous Agent Template
Date: 2026-08-23
Status: Template — awaiting owner configuration

## What This Is

This repo is a template for an autonomous social media agent. The agent runs on GitHub Actions and posts to X and/or Bluesky automatically. But first, the owner must configure it.

## Required Setup Steps

### Step 1: Fill in ME.md
Open `ME.md` and replace all `[placeholder]` values with real information:
- Your name and location
- Your background and expertise
- Your current role and company
- Your expertise areas (these become content pillars)
- Your GitHub, LinkedIn, X, Bluesky profile URLs

This is the single most important file. Without it, the agent has no identity and cannot create relevant content.

### Step 2: Set GOALS.md
Open `GOALS.md` and define:
- What you're trying to achieve (followers, newsletter subscribers, GitHub stars, etc.)
- Your numeric target
- Your deadline
- Your constraints

### Step 3: Configure Credentials

#### X (Twitter) API
Add these GitHub repository secrets:
- `X_API_KEY` — API key from developer.twitter.com
- `X_API_SECRET` — API secret
- `X_ACCESS_TOKEN` — Access token (write permissions required)
- `X_ACCESS_TOKEN_SECRET` — Access token secret

See `agent/integrations/x/README.md` for details.

#### Bluesky
Add these GitHub repository secrets:
- `BLUESKY_HANDLE` — Your handle (e.g., `yourname.bsky.social`)
- `BLUESKY_PASSWORD` — Your app password (create at bsky.app/settings/app-passwords)

See `agent/integrations/bluesky/README.md` for details.

### Step 4: Update Integration Plans
After configuring credentials, update:
- `agent/integrations/x/plan.md` — your X handle, Premium status, follower count
- `agent/integrations/bluesky/plan.md` — your Bluesky handle

### Step 5: Update Content Pillars
Open `agent/memory/pillars.md` and replace the placeholder pillars with your actual expertise areas from ME.md.

### Step 6: Enable GitHub Actions
Make sure GitHub Actions are enabled in your repo settings. The workflows in `.github/workflows/` will run automatically once configured.

## What Happens After Setup

Once all steps are complete:
1. The agent runs on its defined schedule (see `.github/workflows/agent-work.yml`)
2. Each session: researches content, creates posts, pushes to `agent/outputs/{platform}/`
3. The posting workflow picks up files from outputs and publishes them
4. The agent creates PRs for each session, self-reviews, and auto-merges

## Verification Check

The agent will know setup is complete when:
- ME.md has no `[placeholder]` values
- GOALS.md has real numeric targets
- `gh variable list` shows platform credentials configured
- `gh run list --workflow=agent-work.yml` shows successful runs

## Notes

- The agent cannot guess your identity — ME.md must be filled in by a human
- Content quality depends entirely on the quality of ME.md (expertise, angles, voice)
- The more specific ME.md is, the better the agent's content will be
