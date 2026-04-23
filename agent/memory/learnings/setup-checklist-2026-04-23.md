# Setup Checklist for New Repo Owner
Created: 2026-04-23
Status: ACTIVE — owner must complete before agent can create real content

## What the Agent Found
This is a fresh template repository. All key config files contain placeholder content.
The agent cannot create meaningful content until the owner fills in their identity and goals.

## Owner Setup Steps (in order)

### Step 1: Configure GOALS.md
Replace placeholders with your actual goal:
- What metric are you optimizing? (X followers, GitHub stars, newsletter subscribers, etc.)
- What is your numeric target?
- What is your deadline?
- What are your constraints?

### Step 2: Configure ME.md
Replace placeholders with your real info:
- Name, location, background
- Current role and company
- Expertise areas (these become content pillars)
- All your social links (GitHub, X, LinkedIn, Bluesky)
- Your open source projects (the agent will discover and promote these)
- Known live outcomes (blog, newsletter) that the agent should link to

### Step 3: Configure agent/memory/pillars.md
Based on ME.md, define 3-5 content pillars:
- Each pillar = a topic area where you have real expertise and authority
- These are the filters for all content — if a post doesn't connect to a pillar, the agent skips it
- Good pillars: specific enough to be authoritative, broad enough for daily content

### Step 4: Configure Platform Integration Plans
For X: `agent/integrations/x/plan.md`
- Add your @handle
- Note whether you have Premium (affects character limits and reach)
- Set posting frequency targets

For Bluesky: `agent/integrations/bluesky/plan.md`
- Add your handle
- Note posting cadence

### Step 5: Configure GitHub Secrets/Variables
See README.md for required secrets:
- X API credentials (for posting to X)
- Bluesky credentials (for posting to Bluesky)
- Other platform keys as needed

## What Happens After Setup
Once configured, the agent will:
1. Read ME.md → discover your expertise pillars
2. Run web searches for news in those pillars
3. Create content files in `agent/outputs/x/` and `agent/outputs/bluesky/`
4. The GitHub Actions workflow auto-posts those files
5. Metrics are tracked in the state file each session

## Agent Capabilities (Once Running)
- Daily web research on your pillar topics
- 2-3 content pieces per session (posts and replies)
- Building-in-public milestones when you hit goals
- Weekly retrospectives to improve strategy
- Self-correcting based on what performs well

## Note to Future Agent Sessions
Until the owner completes this setup, every session should:
1. Check if GOALS.md still has placeholder content
2. If yes → skip content creation, skip PR (nothing meaningful to commit)
3. If no → proceed with normal content session

Once `GOALS.md` has real content (not "[YOUR GOAL HERE]"), full sessions can begin.
