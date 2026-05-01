# Setup Checklist — First Session
Date: 2026-05-01

## Status: AWAITING OWNER CONFIGURATION

This is a fresh clone of the Autonomous Agent X/Bluesky Template. The agent cannot
operate meaningfully until the owner fills in the core configuration files.

## Required Steps (Owner Must Do These)

### Step 1: Fill in ME.md
File: `ME.md`

Replace all `[placeholder]` values with:
- Your name and location
- Your background and current role
- Your company (if applicable)
- Your expertise areas (be specific — these become content pillars)
- Your current projects
- Your GitHub profile URL (the agent discovers repos from this)
- Your social links (LinkedIn, GitHub, X, Bluesky)
- Content angles for the agent

### Step 2: Define Your Goals
File: `GOALS.md`

Replace all `[placeholder]` values with:
- Your target metric (e.g., "500 X followers", "100 GitHub stars")
- Your deadline (e.g., "3 months from start")
- Start date (today)
- Any constraints specific to your situation

### Step 3: Define Content Pillars
File: `agent/memory/pillars.md`

Replace `[Pillar 1]` etc. with your actual expertise areas. Example:
- Pillar 1: Autonomous AI agents — building and operating agents in production
- Pillar 2: Developer tools — open source tools for developers
- Pillar 3: Startup building — lessons from founding and running companies

Also fill in target communities on X that align with your pillars.

### Step 4: Configure Platform Accounts
Files:
- `agent/integrations/x/plan.md` — Your X handle, Premium status, follower count
- `agent/integrations/bluesky/plan.md` — Your Bluesky handle

### Step 5: Configure GitHub Secrets/Variables
See README.md for required:
- GitHub secrets (API keys for X, Bluesky)
- GitHub variables (MAX_PRS_PER_DAY, etc.)

## After Configuration

Once the above files are filled in, the next agent session will:
1. Read your identity and goals
2. Discover your open source repos from GitHub
3. Research relevant news hooks for your pillars
4. Create initial content posts for X and Bluesky
5. Begin the posting cadence

## Notes for Agent (Future Sessions)

When ME.md and GOALS.md are filled in:
- Delete or archive this checklist file
- The state file's "Blockers" section should be updated
- Begin with discovery skill to understand the owner's context
