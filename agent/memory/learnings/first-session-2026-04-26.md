# First Session Learning: Template Not Configured

Date: 2026-04-26
Session: S001

## Situation

Agent ran for the first time on a fresh template clone. Both `ME.md` and `GOALS.md` contained only placeholder text with no real owner information. X and Bluesky credentials were also not configured.

## What Happened

The agent correctly:
1. Read state files and discovered none existed yet
2. Checked queue counts (both 0)
3. Read ME.md and GOALS.md — found only template placeholders
4. Did NOT create generic/hallucinated content
5. Created the state file with clear blocker documentation
6. Created this learning note

## Key Lesson

**On an unconfigured template, do NOT create placeholder content.**

Generic content wastes queue space and produces no value. The correct action is:
1. Document the blockers clearly in state file
2. Create the state file so future sessions have a starting point
3. Note what the owner needs to do to unblock

## Required Owner Actions (Before Content Can Start)

1. **ME.md** — Replace ALL `[placeholders]` with real info:
   - Name, location, background
   - Current role and company
   - Expertise areas (these become pillars)
   - GitHub URL, X handle, Bluesky handle, LinkedIn
   - Current projects and live outputs

2. **GOALS.md** — Set real targets:
   - Primary metric (followers, stars, subscribers)
   - Target number and deadline
   - Success criteria

3. **GitHub Secrets** (repository settings → Secrets and variables → Actions):
   - `X_API_KEY` + `X_API_SECRET` — from developer.twitter.com
   - `X_ACCESS_TOKEN` + `X_ACCESS_TOKEN_SECRET` — OAuth 1.0a user tokens
   - `BLUESKY_HANDLE` — e.g., `yourname.bsky.social`
   - `BLUESKY_APP_PASSWORD` — from Bluesky Settings → App Passwords
   - `ANTHROPIC_API_KEY` — from console.anthropic.com
   - `GH_TOKEN` — GitHub PAT with repo scope

4. **agent/memory/pillars.md** — Replace placeholder pillar table with real pillars (or let agent discover from ME.md on first real session)

## What Should Happen Next Session

Once ME.md and GOALS.md are configured:
1. Agent reads ME.md → discovers expertise pillars
2. Agent reads GOALS.md → sets target metrics in state file
3. Agent runs discovery skill → finds owner's GitHub repos, live outputs
4. Agent does web research → finds timely news hooks for pillars
5. Agent creates 2-3 content pieces for X + Bluesky versions
6. Agent updates pillars.md with discovered pillars

## Status
- Blockers documented in: `agent/state/current.md`
- Template ready for owner customization
