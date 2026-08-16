# Setup Notes — 2026-08-16

## Status
This is a fresh template repository. The following items must be completed by the repo owner before the agent can operate meaningfully.

## Required Owner Actions (in order)

### 1. Fill in ME.md
- Your name, location, background
- Current role and company
- Expertise areas (these become content pillars)
- GitHub profile URL (agent scans it for projects to promote)
- All social links (X handle, LinkedIn, Bluesky)

### 2. Fill in GOALS.md
- What metric you want to grow (followers, GitHub stars, newsletter subscribers)
- Numeric target
- Deadline
- Constraints

### 3. Update agent/memory/pillars.md
- Based on your ME.md expertise areas
- 3-5 pillars that represent your real knowledge
- Target X communities for each pillar

### 4. Configure GitHub Secrets
Required secrets (Settings → Secrets and variables → Actions):
- X API: `X_API_KEY`, `X_API_SECRET`, `X_ACCESS_TOKEN`, `X_ACCESS_TOKEN_SECRET`
- Bluesky: `BLUESKY_HANDLE`, `BLUESKY_APP_PASSWORD`
- GitHub: `GH_TOKEN` (fine-grained PAT for PR creation)

### 5. Update Integration Plan Files
- `agent/integrations/x/plan.md` — add your handle, follower count, premium status
- `agent/integrations/bluesky/plan.md` — add your handle

### 6. Review Workflow Schedule
- `.github/workflows/agent-work.yml` — adjust cron schedule to your timezone/preferences
- Default is 9 sessions/day

## What the Agent Can Do Once Configured
- Research daily AI/tech news and filter through your content pillars
- Write X posts (Premium length: 500-1000 chars for most types)
- Write separate Bluesky posts (under 290 chars)
- Auto-post via GitHub Actions
- Track metrics, queue counts, and session history
- Self-improve via weekly retrospectives
- Create and self-review PRs

## Queue System
- Posts go to `agent/outputs/x/` and `agent/outputs/bluesky/`
- Workflows auto-post and move files to `posted/`
- Queue hard limit: 15 files per platform (agent self-enforces)
- At queue >= 13: agent stops creating content automatically

## Notes
- Example content files in outputs/ are labeled "EXAMPLE POST — DELETE BEFORE GOING LIVE"
- Delete them once you've configured the agent and are ready to go live
- The agent will create real content once it has your identity and goals
