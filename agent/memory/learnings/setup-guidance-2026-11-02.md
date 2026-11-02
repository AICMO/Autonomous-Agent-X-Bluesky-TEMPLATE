# Setup Guidance: Getting Started with This Template

Date: 2026-11-02
Status: Reference document for first agent session

## What This Agent Needs to Operate

This document captures what the agent discovered on its first session: the repository is a template with no owner configuration. Before the agent can create content or pursue goals, the owner must complete setup.

## Required Steps (In Order)

### 1. Fill in ME.md (Most Important)

ME.md is the foundation. The agent reads this to understand:
- Who the owner is (name, background)
- What they know (expertise areas)
- What they're building (current projects)
- Where to link (GitHub, X, LinkedIn, Bluesky)
- What angles to use for content

**Without ME.md, the agent has no identity to write from.**

### 2. Define Goals in GOALS.md

GOALS.md tells the agent:
- What metric to grow (followers, stars, subscribers)
- The target number
- The deadline
- Any constraints

**Without GOALS.md, the agent has no direction.**

### 3. Configure Platform Credentials

For X (Twitter):
- Set `X_API_KEY`, `X_API_SECRET`, `X_ACCESS_TOKEN`, `X_ACCESS_TOKEN_SECRET` as GitHub secrets
- Set `X_USER_ID` as a GitHub variable
- Update `agent/integrations/x/plan.md` with handle and follower count

For Bluesky:
- Set `BLUESKY_HANDLE` and `BLUESKY_APP_PASSWORD` as GitHub secrets
- Update `agent/integrations/bluesky/plan.md` with handle and follower count

### 4. Let the Agent Discover Pillars

Once ME.md and GOALS.md are filled in, the agent will automatically:
- Read expertise areas from ME.md
- Map them to content pillars
- Create `agent/memory/pillars.md`
- Start creating targeted content

## What Happens After Setup

Once configured, the agent will follow this cycle each session:
1. Check state file and recent PRs
2. Research news relevant to content pillars
3. Create 2-5 content pieces (X posts + Bluesky versions)
4. Queue them for auto-posting via GitHub Actions
5. Create a PR with all changes

The `process-outputs.yml` workflow automatically posts queued content to X and Bluesky.

## Key Principles to Know

- **Queue limit**: Never queue more than 15 posts per platform. The agent enforces this.
- **Content is lost without PRs**: All content must be committed to git to be posted.
- **One PR per session**: The agent creates exactly one PR per work session.
- **Weekly retros**: Every Sunday the agent runs a deeper analysis and updates its skills.

## Links

- See `README.md` for full setup guide
- See `CLAUDE.md` for agent operating instructions
- See `agent/config.md` for safety boundaries
