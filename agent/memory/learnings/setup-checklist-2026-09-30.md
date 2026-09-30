# Setup Checklist — Template Repo Initial State
Date: 2026-09-30
Status: AWAITING OWNER CONFIGURATION

## Summary

This repo was cloned from the Autonomous-Agent-X-Bluesky-TEMPLATE. All configuration files are placeholders. The agent cannot produce real content until the owner fills in the required files.

---

## Required Configuration (Must complete in order)

### 1. ME.md — Owner Identity
File: `ME.md`
What to fill in:
- Name, location, background
- Current role and company
- Expertise areas (at least 3)
- Current projects
- GitHub profile URL (the agent scans this to discover repos)
- LinkedIn, X, Bluesky links
- Content angles (perspectives the agent should write from)

**Why it matters:** Every content pillar and opinion piece is grounded in the owner's real expertise. Without this, content is generic and low-value.

### 2. GOALS.md — Success Targets
File: `GOALS.md`
What to fill in:
- Primary metric (followers, stars, subscribers, etc.)
- Numeric target (e.g., 1,000 followers)
- Deadline (e.g., 90 days from start date)
- Start date
- Constraints (organic only, ethical only, etc.)

**Why it matters:** The agent tracks velocity and ETA against this target. Without a goal, every session is undirected.

### 3. Content Pillars
File: `agent/memory/pillars.md`
What to fill in:
- 3-5 expertise pillars (discovered from ME.md)
- Target communities on X (find via x.com/i/communities)
- Join communities manually in X UI (cannot be done via API)

**Why it matters:** Every post must connect to a pillar. Without pillars, the agent posts off-topic content that doesn't build audience authority.

### 4. Platform Integration Plans
Files:
- `agent/integrations/x/plan.md` — Add your X handle, follower count, Premium status, posting limits
- `agent/integrations/bluesky/plan.md` — Add your Bluesky handle

**Why it matters:** The publishing skill checks these files for current limits and drain rates.

### 5. GitHub Secrets and Variables
Required secrets (set in repo Settings → Secrets → Actions):
- X credentials: `X_API_KEY`, `X_API_SECRET`, `X_ACCESS_TOKEN`, `X_ACCESS_SECRET` (and/or `X_BEARER_TOKEN`)
- Bluesky credentials: `BLUESKY_HANDLE`, `BLUESKY_APP_PASSWORD`
- Anthropic key: `ANTHROPIC_API_KEY`

Check `README.md` for the full required secrets list and any repo/org-level settings needed (rulesets, Actions permissions).

**Verification:** Run `gh variable list` — if variables exist, presume secrets are also set.

### 6. Workflow Schedule (Optional Tuning)
File: `.github/workflows/agent-work.yml`
Default crons run multiple times per day. Adjust to your preference.

---

## What Happens After Configuration

Once all files are filled in, the next agent session will:
1. Run the discovery skill to scan owner's GitHub and discover repos/live outputs
2. Confirm or update pillars in `agent/memory/pillars.md`
3. Research current AI news filtered through the pillars
4. Create 5-8 content pieces (X + Bluesky) targeting engagement
5. Begin tracking metrics toward the GOALS.md target

---

## Quick Verification Checklist

Before expecting real content output, verify:
- [ ] ME.md has real name, background, expertise (no `[placeholders]`)
- [ ] GOALS.md has real target metric and deadline
- [ ] agent/memory/pillars.md has 3+ real pillars
- [ ] agent/integrations/x/plan.md has real handle and follower count
- [ ] GitHub secrets are configured (check Actions tab for successful runs)
- [ ] agent/state/current.md has no active blockers

---

## Agent Behavior When Unconfigured

When this agent runs without configuration, it:
1. Detects that all files are placeholders
2. Documents the setup requirements (this file)
3. Creates/updates the state file
4. Creates a PR to preserve the work
5. Does NOT generate fake placeholder content that would pollute the queue

This is correct behavior — partial setup is documented, not silently ignored.
