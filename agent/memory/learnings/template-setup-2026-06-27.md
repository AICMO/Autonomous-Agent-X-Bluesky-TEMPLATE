# Template Setup Guide
Date: 2026-06-27
Session: S1 (First session on fresh template)

## Context
This repository was cloned from the Autonomous-Agent-X-Bluesky-TEMPLATE. All key configuration files contain placeholder content and must be filled in by the repo owner before the agent can operate effectively.

## Required Owner Actions (in order)

### 1. Fill in ME.md (HIGHEST PRIORITY)
The agent uses ME.md as its primary source of truth for:
- Who the author is (name, background, expertise)
- What content pillars to use
- What to promote (repos, company, links)
- Personal voice and angles

**What to add:**
- Real name and location
- Actual background and current role
- Real expertise areas (these become content pillars)
- GitHub profile URL (agent scans this for repos to promote)
- LinkedIn, X, Bluesky profile URLs
- Company name, website, what it does
- Content angles specific to your experience

### 2. Fill in GOALS.md (HIGH PRIORITY)
The agent uses GOALS.md to know what success looks like.

**What to add:**
- Primary growth metric (followers, newsletter subscribers, GitHub stars, etc.)
- Specific numeric target (e.g., "1000 followers")
- Deadline
- Start date
- Any constraints (posting frequency, topics to avoid)

### 3. Update agent/memory/pillars.md (HIGH PRIORITY)
After ME.md is configured, either:
- Let the agent discover pillars from ME.md next session (it will create a real pillars.md), OR
- Manually fill in 3-5 content pillars from your expertise

### 4. Configure Platform Integrations
See README.md for instructions on setting up:
- X (Twitter) API credentials
- Bluesky credentials
- GitHub Actions secrets

## What Happens After Configuration

Once ME.md and GOALS.md are filled in, the agent will:
1. Discover content pillars from your expertise areas
2. Research relevant AI/tech news that connects to your pillars
3. Create 2-5 content pieces per session (X posts + Bluesky versions)
4. Create engagement replies to build audience
5. Track metrics and iterate based on what works

## Key Files Reference
| File | Purpose | Status |
|------|---------|--------|
| `ME.md` | Owner identity, expertise, links | NEEDS SETUP |
| `GOALS.md` | Growth targets, success criteria | NEEDS SETUP |
| `agent/memory/pillars.md` | Content lanes (expertise areas) | NEEDS SETUP |
| `agent/state/current.md` | Session tracking, metrics | CREATED |
| `agent/integrations/x/plan.md` | X account status, limits | NEEDS REAL DATA |
| `agent/integrations/bluesky/plan.md` | Bluesky account status | NEEDS REAL DATA |

## Notes for Agent (Next Session)
- If ME.md and GOALS.md are still placeholders, create NO content. Document status.
- If ME.md is filled in, discover pillars and update `agent/memory/pillars.md`
- If both are filled in and pillars are defined, begin content creation cycle
- Always verify queue counts before creating content (even in first real session)
