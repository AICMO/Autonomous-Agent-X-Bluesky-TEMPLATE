# Learning: Template Setup Requirements
Date: 2026-07-14
Session: S1 (First Session)
Status: Active — awaiting owner configuration

## Context
This is the inaugural session of the Autonomous-Agent-X-Bluesky-TEMPLATE. The repository is a clean template with all infrastructure in place but no owner-specific content configured yet.

## What's Ready (No Action Needed)
- All GitHub Actions workflows: agent-work.yml, agent-review.yml, agent-work-trigger.yml, process-outputs.yml, owner-reminder.yml
- All skill files: publishing, commenting, discovery, integrations
- All memory directories: research/, hypotheses/, learnings/, plans/
- Platform integration templates: agent/integrations/x/plan.md, agent/integrations/bluesky/plan.md
- Content pillars template: agent/memory/pillars.md
- CLAUDE.md operating instructions (fully detailed)

## What Owner Must Configure

### Priority 1: Identity (ME.md)
Fill in with real data:
- Full name, location, background
- Current role and company
- Expertise areas (these become content pillars)
- GitHub profile URL (for discovery skill to scan)
- LinkedIn, X, Bluesky, GitHub links
- Content angles (perspectives the agent should write from)
- Known live outputs (blog, newsletter URLs)

### Priority 2: Goals (GOALS.md)
Define measurable targets:
- Which metric to track (followers, stars, subscribers)
- Numerical target
- Deadline/timeframe
- Growth constraints
- Success criteria (primary + secondary)

### Priority 3: Platform Credentials (GitHub Secrets)
Required for posting:
- `ANTHROPIC_API_KEY` — Required for all agent sessions
- `X_API_KEY`, `X_API_SECRET`, `X_ACCESS_TOKEN`, `X_ACCESS_TOKEN_SECRET` — For X posting
- `BLUESKY_HANDLE`, `BLUESKY_APP_PASSWORD` — For Bluesky posting

### Priority 4: Platform Plan Files
Update with real account data:
- `agent/integrations/x/plan.md` — Real handle, follower count, Premium tier status
- `agent/integrations/bluesky/plan.md` — Real handle, follower count

### Priority 5: Content Pillars
After ME.md is filled:
- Update `agent/memory/pillars.md` with real expertise areas
- These should come from ME.md expertise areas and GOALS.md purpose
- 3-5 pillars recommended

## What Happens After Configuration
Once ME.md and GOALS.md are filled and credentials are set:
1. Agent can discover content pillars from owner's expertise
2. Agent can find promotable repos via GitHub profile scan
3. Agent can research timely news and filter through pillars
4. Agent can create posts that connect news hooks to owner's expertise
5. Agent can track progress toward defined goal

## Key Insight for Template Users
**The agent is as good as the ME.md file.** The better the owner describes their expertise, projects, and angles — the better the agent can write in their voice and represent their perspective. Spend 30 minutes filling in ME.md thoroughly. It's the highest-leverage action available before the first real content session.

## Template Files NOT to Modify
These are instructions, not config — leave them as-is:
- CLAUDE.md (operating instructions)
- .claude/skills/*.md (all skill files)
- agent/config.md (boundaries)
- .github/workflows/*.yml (automation)

## Next Steps (for Owner)
1. Fork this repo (if not done)
2. Fill in ME.md
3. Fill in GOALS.md
4. Add GitHub secrets (ANTHROPIC_API_KEY minimum)
5. Enable GitHub Actions
6. Optionally add X/Bluesky credentials
7. Trigger first content session: `gh workflow run agent-work.yml`
