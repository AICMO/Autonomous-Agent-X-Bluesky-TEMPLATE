# Setup Checklist — Template Configuration Required
Date: 2026-08-30
Status: Pending owner action

## Overview

This agent detected that the repository is in its unconfigured template state. The following steps are required before the agent can begin autonomous content creation.

---

## Required Configuration Steps

### Step 1: Fill in ME.md
**File:** `ME.md` (repo root)

Replace ALL placeholder values with real information:
- Your name and location
- Your background and current role
- Your company (if applicable)
- Your expertise areas (these become content pillars)
- Your current projects
- Your GitHub profile URL (agent will scan this each session)
- Your social links (LinkedIn, X, Bluesky)
- Content angles — how you want to be positioned

**Why this matters:** ME.md is the agent's primary source for:
- Content pillars (what to post about)
- CTAs and links (what to promote)
- Voice and positioning (how to sound)

---

### Step 2: Fill in GOALS.md
**File:** `GOALS.md` (repo root)

Set a concrete, measurable goal:
```markdown
# Goal: Reach 1,000 X followers

## Target
- Metric: X Followers
- Target: 1,000
- Deadline: 6 months from start
- Start Date: 2026-09-01

## Constraints
- Organic growth only
- Ethical strategies only
- Post only on topics related to [your expertise]

## Success Criteria
- 1,000 genuine followers who engage with content
- Average engagement rate > 1.5%
```

**Why this matters:** GOALS.md sets the agent's direction. Without a goal, the agent cannot prioritize or measure progress.

---

### Step 3: Configure GitHub Secrets
**Location:** Repository Settings → Secrets and Variables → Actions

#### X (Twitter) API Credentials
Required secrets:
- `X_API_KEY` — from developer.twitter.com
- `X_API_SECRET` — from developer.twitter.com
- `X_ACCESS_TOKEN` — from developer.twitter.com
- `X_ACCESS_TOKEN_SECRET` — from developer.twitter.com

To get X API access:
1. Apply at developer.twitter.com/en/portal/petition/essential/basic-info
2. Create a new app
3. Enable "Read and Write" permissions
4. Generate Access Token and Secret from the "Keys and Tokens" tab

#### Bluesky Credentials
Required secrets:
- `BLUESKY_HANDLE` — your handle (e.g., `yourname.bsky.social`)
- `BLUESKY_PASSWORD` — an App Password (not your main password)

To create a Bluesky App Password:
1. Go to Settings → Privacy and Security → App Passwords
2. Create a new app password named "agent"
3. Copy the password immediately (only shown once)

---

### Step 4: Configure GitHub Variables
**Location:** Repository Settings → Secrets and Variables → Actions → Variables

Optional but recommended:
- `MAX_PRS_PER_DAY` — default is 10, reduce if you want fewer agent sessions per day

---

### Step 5: Update Platform Plans
After configuring credentials, update these files:
- `agent/integrations/x/plan.md` — add your @handle, follower count, Premium status
- `agent/integrations/bluesky/plan.md` — add your handle

---

### Step 6: Update Content Pillars
**File:** `agent/memory/pillars.md`

After filling in ME.md, either:
- Manually fill in pillars based on your expertise areas, OR
- Let the agent discover pillars from ME.md on its next session

---

## What Happens After Configuration

Once the above steps are complete, the agent will:
1. Read ME.md to discover content pillars
2. Research trending topics in your expertise areas
3. Create 2-5 content pieces per session
4. Stage them to `agent/outputs/x/` and `agent/outputs/bluesky/`
5. The GitHub Actions workflow will automatically post them to X and Bluesky
6. Track metrics and adjust strategy over time

---

## Current State Summary

| Item | Status |
|------|--------|
| ME.md | Unconfigured (template placeholders) |
| GOALS.md | Unconfigured (template placeholders) |
| X credentials | Not configured |
| Bluesky credentials | Not configured |
| Content queue (X) | 0 files |
| Content queue (Bluesky) | 0 files |
| agent/state/current.md | Created (this session) |
| agent/memory/pillars.md | Template only |

---

## References
- `README.md` — Full setup and architecture documentation
- `CLAUDE.md` — Agent operating instructions
- `agent/config.md` — Agent boundaries and limits
- `agent/integrations/x/README.md` — X integration details
- `agent/integrations/bluesky/README.md` — Bluesky integration details
