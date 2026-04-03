# Template Setup Checklist
Created: 2026-04-03
Status: PENDING — awaiting owner configuration

## What Needs to Be Done Before Agent Can Operate

### Owner Actions Required

1. **ME.md** — Replace all `[placeholder]` values with real info:
   - Name, location, background
   - Current role and company
   - Expertise areas (these become content pillars)
   - Links (GitHub, X, LinkedIn, Bluesky)
   - Content angles for the agent

2. **GOALS.md** — Define the actual goal:
   - What metric to grow (followers, stars, subscribers)
   - Target number
   - Deadline
   - Constraints

3. **GitHub Secrets** — Configure at repo Settings > Secrets > Actions:
   - For X: `X_API_KEY`, `X_API_SECRET`, `X_ACCESS_TOKEN`, `X_ACCESS_TOKEN_SECRET`
   - For Bluesky: `BLUESKY_HANDLE`, `BLUESKY_APP_PASSWORD`

4. **pillars.md** — Update `agent/memory/pillars.md` with real content pillars based on ME.md expertise

5. **Integration Plans** — Update:
   - `agent/integrations/x/plan.md` — add handle, follower count, Premium status
   - `agent/integrations/bluesky/plan.md` — add handle

### Agent Actions (Once Owner Completes Above)

1. Run discovery skill to research owner's background and online presence
2. Create first research file on pillar-relevant news
3. Create first 2-3 content pieces
4. Establish posting rhythm

## Key Insight
Without ME.md and GOALS.md configured, content creation is impossible — there are no pillars, no voice, no target audience defined. The agent correctly identified this and documented it rather than creating generic placeholder content.
