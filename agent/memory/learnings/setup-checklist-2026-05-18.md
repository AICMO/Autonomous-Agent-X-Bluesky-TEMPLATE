# Learning: Template Setup Checklist
Date: 2026-05-18
Session: S1 (first session)
Status: Active guidance

## Context

This repo was just initialized from the Autonomous-Agent-X-Bluesky-TEMPLATE. The agent ran its first session and found all config files are unfilled placeholders. This document captures what's needed before the agent can operate.

## Required Setup Steps (In Order)

### Step 1: Configure Identity (ME.md)
The agent reads ME.md to understand:
- Who the owner is (name, background, expertise)
- What to promote (GitHub repos, projects, company)
- Content angles (what perspectives to write from)
- Social links (X, Bluesky, LinkedIn, GitHub)

Without ME.md, the agent cannot create relevant content.

**Reference:** Live example at https://github.com/AICMO/Autonomous-Agent-X-Bluesky/blob/main/ME.md

### Step 2: Configure Goals (GOALS.md)
The agent reads GOALS.md to understand:
- What metric to grow (followers, stars, subscribers)
- Target number and deadline
- Constraints (organic only, ethical strategies, etc.)

Without GOALS.md, the agent has no direction.

**Reference:** Live example at https://github.com/AICMO/Autonomous-Agent-X-Bluesky/blob/main/GOALS.md

### Step 3: Add Secrets (GitHub Settings → Secrets)
Minimum required:
- `ANTHROPIC_API_KEY` — Powers the Claude agent

For X posting:
- `X_API_KEY`, `X_API_SECRET`, `X_ACCESS_TOKEN`, `X_ACCESS_TOKEN_SECRET`, `X_BEARER_TOKEN`

For Bluesky posting:
- `BLUESKY_HANDLE`, `BLUESKY_PASSWORD`

### Step 4: Configure Repository
- Add branch ruleset (see README.md → Setup → Branch Ruleset)
- Enable workflow permissions (Actions → General → Read and write)

### Step 5: Enable Workflows
GitHub disables workflows when using a template or forking.
Go to Actions tab → enable all workflows.

### Step 6: Run First Real Session
```bash
gh workflow run agent-work.yml
```

## What Happens After Setup

Once ME.md and GOALS.md are filled:
1. Agent discovers content pillars from owner's expertise
2. Agent creates `agent/memory/pillars.md` with active pillars
3. Agent creates integration plan files for X and Bluesky
4. Agent begins creating content targeting the configured goal
5. Posting workflows auto-post content every 2 hours

## Key Insight

The agent is fully autonomous once configured. The owner's only ongoing job is:
- Optionally provide analytics data (via GitHub Issues created each Saturday)
- Review and merge any PRs if auto-merge isn't enabled

Everything else — research, content creation, posting, self-improvement — is handled automatically.
