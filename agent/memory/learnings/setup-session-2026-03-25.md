# Learning: Template Setup Session
Date: 2026-03-25
Session: S1 (first ever)

## Context
This is a fresh fork/clone of the Autonomous-Agent-X-Bluesky-TEMPLATE. The owner has not yet configured the required personal files.

## Files Needing Configuration

### Required (before content creation):
1. **ME.md** — Must fill in:
   - Name, location, background
   - Current role and company
   - Expertise areas (these become content pillars)
   - Current projects
   - Social media links (X, LinkedIn, GitHub, Bluesky)
   - Content angles

2. **GOALS.md** — Must fill in:
   - Primary metric and target number
   - Deadline/timeframe
   - Success criteria

### Recommended (for actual posting):
3. X API credentials (secrets): `X_API_KEY`, `X_API_KEY_SECRET`, `X_ACCESS_TOKEN`, `X_ACCESS_TOKEN_SECRET`
4. Bluesky credentials: `BLUESKY_HANDLE` (variable), `BLUESKY_APP_PASSWORD` (secret)

### Optional but useful:
5. `AGENT_PAT` secret for autonomous loop (without it, sessions don't auto-trigger after merges)
6. `MAX_PRS_PER_DAY` variable (default: 2)

## What Happens Next Session

If ME.md and GOALS.md are still empty:
- Continue documenting the setup state
- Do NOT attempt to create content with placeholder data

If ME.md and GOALS.md are filled in:
1. Read both files thoroughly
2. Discover and update `agent/memory/pillars.md` with owner's actual expertise pillars
3. Research current news/trends in pillar topics
4. Create first batch of 5-8 real content pieces

## Reference
See README.md Quick Start section for full setup instructions.
Live example: https://github.com/AICMO/Autonomous-Agent-X-Bluesky
