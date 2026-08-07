# Learning: Template Repository — First Session

Date: 2026-08-07
Session: S1 (first session)

## Context

This is the first agent session on this repository. ME.md and GOALS.md contain only template placeholder content — no real user identity or goals have been configured.

## Finding

**Content creation is impossible until ME.md and GOALS.md are configured.**

The publishing skill requires:
1. Owner identity → determines content voice, expertise angles, links to promote
2. Expertise pillars → gates every piece of content (skip if no pillar connection)
3. Goals → determines what metrics to optimize (follower growth? engagement? stars?)

Without these, any content produced would be generic and off-brand.

## What the Repo Owner Must Do

### Step 1: Fill in ME.md
Replace every `[placeholder]` with real values:
- Real name, location, background
- Current role and what you're building
- Expertise areas (AI/ML? SaaS? Healthcare? Finance? etc.) — these become content pillars
- GitHub profile URL (the agent scans this to find promotable repos)
- Social links: X handle, Bluesky handle, LinkedIn

### Step 2: Fill in GOALS.md
Replace every `[placeholder]` with measurable targets:
- Which metric: e.g., "X Followers" or "GitHub Stars on [repo]"
- Target number: e.g., 1000 followers
- Deadline: e.g., 90 days from 2026-08-07 = 2026-11-05
- Success criteria: primary + secondary

### Step 3: Configure GitHub Secrets (optional but recommended)
If you want the agent to actually post to platforms:
- X: X_API_KEY, X_API_SECRET, X_ACCESS_TOKEN, X_ACCESS_TOKEN_SECRET
- Bluesky: BLUESKY_HANDLE (variable), BLUESKY_APP_PASSWORD (secret)

### Step 4: Set MAX_PRS_PER_DAY variable
Recommended starting value: 3-5 per day while testing.

## What Happens Next Session (After Configuration)

1. Agent reads ME.md → discovers expertise pillars → creates `agent/memory/pillars.md`
2. Agent reads GOALS.md → sets target metric in state file
3. Agent scans GitHub profile for promotable repos
4. Agent creates first content batch (5-8 pieces) aligned to pillars and goals
5. Content queues in `agent/outputs/x/` and `agent/outputs/bluesky/`
6. Workflows post content at configured rate

## Template State Summary

```
ME.md: TEMPLATE (all placeholders)
GOALS.md: TEMPLATE (all placeholders)
agent/state/current.md: CREATED (this session)
agent/outputs/x/: EMPTY (0 files)
agent/outputs/bluesky/: EMPTY (0 files)
agent/memory/pillars.md: NOT CREATED (needs ME.md first)
```

## Action for Next Session

If ME.md and GOALS.md are still templates: document blockers, skip content creation, exit.
If ME.md and GOALS.md are configured: create pillars.md, start content creation immediately.
