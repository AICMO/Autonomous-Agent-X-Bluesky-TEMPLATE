# Setup Checklist — Template Configuration Required
Created: 2026-04-17
Status: PENDING (owner action required)

## What Was Found
On first agent session (2026-04-17), all key configuration files contain placeholder values:
- `ME.md` — No real owner identity
- `GOALS.md` — No real goals or metrics
- `agent/memory/pillars.md` — No real content pillars
- `agent/integrations/x/plan.md` — No real X account details
- `agent/integrations/bluesky/plan.md` — No real Bluesky account details
- X credentials: Not configured (session prompt confirms "X credentials not configured")

## Required Owner Actions (In Order)

### Step 1: Identity & Goals (High Priority)
- [ ] Fill in `ME.md` — name, background, expertise areas, current projects, links (LinkedIn, GitHub, X, Bluesky)
- [ ] Fill in `GOALS.md` — real target metric, number, deadline, start date, success criteria
- [ ] Update `agent/memory/pillars.md` — 3-4 real content pillars based on your expertise + goals

### Step 2: Platform Credentials (Required for posting)
See `agent/integrations/x/README.md` and `agent/integrations/bluesky/README.md` for specific setup instructions.

**For X (Twitter):**
- GitHub Secret: `X_API_KEY`, `X_API_SECRET`, `X_ACCESS_TOKEN`, `X_ACCESS_TOKEN_SECRET` (or Bearer Token)
- GitHub Variable: `MAX_PRS_PER_DAY` (recommended: 10)

**For Bluesky:**
- GitHub Secret: `BLUESKY_HANDLE`, `BLUESKY_PASSWORD` (App Password)

### Step 3: Account Details
- [ ] Update `agent/integrations/x/plan.md` — real handle, follower count, Premium status, posting limits
- [ ] Update `agent/integrations/bluesky/plan.md` — real handle, posting config

### Step 4: Verify Workflow
- [ ] Check GitHub Actions are enabled for the repo
- [ ] Verify `agent-work.yml` cron schedule matches your desired posting frequency
- [ ] Run a test dispatch: `gh workflow run agent-work.yml`

## After Configuration
Once the above is complete, the agent will:
1. Auto-detect real pillars from ME.md on next session
2. Create real content based on actual expertise
3. Post to configured platforms
4. Track metrics against real GOALS.md targets

## Notes
- Do NOT create content with placeholder values — posts would be meaningless
- The agent correctly detected the unconfigured state and did NOT attempt to create fake content
- This checklist should be deleted or marked DONE once configuration is complete
