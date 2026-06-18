# Setup Guidance: First Session on Template Repo
Date: 2026-06-18
Status: REFERENCE — for agent use when bootstrapping new installations

## What Was Found
This repo was in a pure template state:
- `ME.md` — all placeholder brackets, no real owner data
- `GOALS.md` — placeholder goal structure, no real targets
- `agent/memory/pillars.md` — placeholder pillars, no real content lanes
- `agent/state/current.md` — did not exist (created this session)
- X queue: 0 files
- Bluesky queue: 0 files
- No research, no learnings, no hypotheses

## Bootstrap Decision
Cannot create useful content without owner persona. Creating generic or made-up content would:
1. Violate anti-AI writing rules (no real specifics = AI slop)
2. Risk being posted to actual social accounts with wrong persona
3. Waste future sessions cleaning up misaligned content

**Correct action: Initialize state, document blockers, create PR. Wait for owner config.**

## What the Owner Must Do
Before the agent can create content:

### 1. Fill in ME.md
Key fields needed:
- Name and background
- Current role and company
- Expertise areas (these become pillars)
- GitHub profile URL (for repo discovery)
- Social links (X, Bluesky, LinkedIn)
- Current projects
- Live outputs (blog, newsletter if any)

### 2. Fill in GOALS.md
Key fields needed:
- Primary metric (followers, GitHub stars, etc.)
- Target number
- Deadline/timeframe
- Constraints specific to this account

### 3. Configure GitHub Secrets/Variables
Required for posting:
- X API credentials (check README.md for exact variable names)
- Bluesky credentials (check README.md)
- Verify with `gh variable list`

### 4. (Optional) Update pillars.md
The agent can auto-generate pillars from ME.md, but owner can pre-seed if they have clear content lanes in mind.

## What Happens After Configuration
Once ME.md and GOALS.md are filled:
1. Agent reads owner background, discovers pillars
2. Agent updates `agent/memory/pillars.md` with real content lanes
3. Agent begins standard content creation cycle
4. Content creation: 2 X posts + 2 Bluesky posts per session (while queue <= 10)

## Key Files to Read at Session Start
(After configuration is complete)
1. `GOALS.md` — current objective
2. `ME.md` — owner persona for content angle
3. `agent/state/current.md` — queue counts, planned steps, blockers
4. `agent/memory/pillars.md` — content lanes
5. `.claude/skills/publishing/SKILL.md` — publishing rules

## Lesson Learned
**First session on a fresh template should be treated as a bootstrap session.** The priority is:
1. Verify configuration state
2. Initialize state file
3. Document what's missing
4. Create PR so the owner can see the blocker clearly

Do NOT attempt content creation on an unconfigured template. The content will be meaningless at best, harmful at worst (if auto-posted with wrong persona).
