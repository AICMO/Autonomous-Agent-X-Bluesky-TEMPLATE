# Setup Checklist — Template Bootstrapping
Date: 2026-06-06
Status: Awaiting owner configuration

## What This Is

This agent repo is a fresh template. On 2026-06-06, the agent ran its first session and found all configuration files contain placeholder values. The agent cannot create useful content or engage authentically until the owner completes setup.

## Required Owner Actions (in order)

### Step 1: Define Identity (ME.md)
Fill in:
- Name, location, background
- Current role and company
- Expertise areas (these become content pillars)
- GitHub profile URL (agent will scan to discover repos/orgs)
- Links (LinkedIn, X, Bluesky)
- Content angles for the agent

### Step 2: Set Goals (GOALS.md)
Fill in:
- What metric to grow (followers, stars, subscribers, etc.)
- Target number and deadline
- Constraints (what the agent must NOT do)
- Success criteria

### Step 3: Configure Platform Integrations
For X (`agent/integrations/x/plan.md`):
- X handle (@username)
- Premium tier status
- Current follower count

For Bluesky (`agent/integrations/bluesky/plan.md`):
- Bluesky handle
- Current follower count

### Step 4: Set GitHub Secrets/Variables
Per README.md, configure:
- X API credentials (for auto-posting)
- Bluesky credentials (for auto-posting)
- Other required variables

### Step 5: Define Content Pillars (`agent/memory/pillars.md`)
Fill in:
- 3-5 pillar topics matching the owner's expertise
- Target X communities for each pillar
- Content angles per pillar

## What Happens After Setup

Once ME.md and GOALS.md are filled in, the next agent session will:
1. Run the discovery skill to understand owner's work, repos, and domain
2. Research top voices in the owner's domain
3. Create first batch of content (5-8 pieces) aligned to pillars
4. Begin engagement strategy

## Notes for the Agent

If you are reading this in a future session and ME.md/GOALS.md still have placeholder values:
- Do NOT attempt to create content (no pillars = no pillar gate to pass)
- Update the state file to reflect blockers
- Create a PR documenting the blocked state
- This is a legitimate outcome — better to stop cleanly than create off-pillar content
