# Template Setup Guide
Date: 2026-05-02
Status: Reference

## What This Is
This file documents the initial state of the Autonomous Agent X/Bluesky template
and the steps needed to configure it for a new owner.

## Required Setup Steps (Owner Must Complete)

### Step 1: Fill in ME.md
The agent reads ME.md every session to understand who it's representing.
Required fields:
- Name and background
- Expertise areas (these become content pillars)
- X handle and Bluesky handle
- GitHub profile URL (agent discovers repos from here)
- Company/project info
- Links (LinkedIn, GitHub, X, Bluesky)

### Step 2: Fill in GOALS.md
The agent needs a clear, measurable goal.
Required fields:
- Target metric (e.g., "X Followers", "GitHub Stars")
- Target number (e.g., 1000 followers)
- Deadline (e.g., "3 months from start")
- Start date

### Step 3: Configure agent/memory/pillars.md
Define 3-5 content pillars based on ME.md expertise.
Each pillar should be:
- An area of genuine expertise
- Something the audience cares about
- Distinct enough that each pillar could stand alone

### Step 4: Update Integration Plan Files
- `agent/integrations/x/plan.md` — Add X handle, verify Premium status
- `agent/integrations/bluesky/plan.md` — Add Bluesky handle

### Step 5: Configure GitHub Secrets/Variables
See README.md for exact variable names needed.
- X API credentials for posting
- Bluesky credentials for posting

## What the Agent Can Do Once Configured
- Research news in owner's expertise pillars daily
- Create 5-8 content pieces per session (X + Bluesky)
- Reply to relevant accounts to build engagement
- Track metrics and adjust strategy
- Self-improve via weekly retrospectives

## Key Files to Know
- `CLAUDE.md` — Full agent operating instructions
- `agent/config.md` — Hard limits and boundaries
- `.claude/skills/publishing/SKILL.md` — Content strategy
- `.claude/skills/commenting/SKILL.md` — Engagement strategy
- `.claude/skills/discovery/SKILL.md` — Research strategy

## Evidence
First session (2026-05-02) found all configuration files in template state.
No content can be created without owner configuration.
