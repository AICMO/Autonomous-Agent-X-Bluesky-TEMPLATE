# Learning: First Run on Unconfigured Template
Date: 2026-06-12
Session: S1 (bootstrap)
Status: Observation

## What Happened

This was the first agent session on a fresh fork of the template. All configuration files contained placeholder content:
- `ME.md`: All `[YOUR_NAME]`, `[YOUR_ROLE]` etc. placeholders
- `GOALS.md`: All `[YOUR GOAL HERE]` placeholders
- `agent/memory/pillars.md`: All placeholder pillar names
- `agent/state/current.md`: Did not exist

Platform credentials were also not configured (X API keys, Bluesky credentials).

## What the Agent Can and Cannot Do Without Configuration

**Can do:**
- Initialize state files and directory structure
- Read and understand the template structure
- Document the unconfigured state
- Run autonomous sessions once configured

**Cannot do without ME.md filled in:**
- Discover content pillars (pillars come from owner expertise in ME.md)
- Write owner-voice content (no identity to write from)
- Find owner's GitHub repos/orgs to promote
- Target communities aligned with owner's domain

**Cannot do without GOALS.md filled in:**
- Track progress against targets
- Calculate velocity or ETA
- Make strategic decisions about content priorities

**Cannot do without credentials:**
- Post content to X or Bluesky
- Read own engagement metrics
- Create reply-to-own sequences

## Minimum Setup Required (from README)

1. Fill in `ME.md` with owner's identity, expertise, links
2. Fill in `GOALS.md` with follower target and deadline
3. Add at minimum `ANTHROPIC_API_KEY` or `CLAUDE_CODE_OAUTH_TOKEN` to repo secrets
4. Configure repo ruleset and workflow permissions per README

## Recommended Setup for Full Functionality

Beyond the minimum:
- X API credentials (4 secrets: API key, API secret, access token, access token secret)
- Bluesky handle (variable) + app password (secret)
- `AGENT_PAT` for autonomous loop chaining
- `MAX_PRS_PER_DAY` variable set to desired session frequency

## Template Design Observation

The template is well-structured with clear separation between:
- Operator config (ME.md, GOALS.md): human fills in once
- Agent runtime state (agent/state/, agent/memory/): agent maintains
- Platform integration (agent/integrations/): hybrid - agent uses but human configures credentials
- Skills (.claude/skills/): agent can update based on evidence

This means the agent can run autonomously indefinitely once the human completes the initial setup — consistent with "Fork → Fill in → Enable → Go" promise in README.
