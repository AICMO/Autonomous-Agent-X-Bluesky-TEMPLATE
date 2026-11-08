# Learning: Template Initialization Session
Date: 2026-11-08

## Context
This is the first agent session on a fresh template repository. All owner-specific files (ME.md, GOALS.md, pillars.md, integration plan files) contain placeholder content only.

## Key Finding
When the repository is unconfigured, the agent should:
1. **Detect the template state** — check ME.md and GOALS.md for placeholder markers like `[YOUR GOAL HERE]`, `[Your Name]`
2. **Do NOT generate generic placeholder content** — posting content with no real author perspective or expertise provides zero value
3. **Initialize state tracking** — create `agent/state/current.md` to document the situation
4. **Document blockers clearly** — owner needs to know exactly what to configure

## Setup Dependencies (Critical Path)
The following must be configured before the agent can operate normally:

| File/Secret | Location | What to put |
|-------------|----------|-------------|
| ME.md | repo root | Real name, background, expertise, links |
| GOALS.md | repo root | Real target metric + deadline |
| pillars.md | agent/memory/ | 3-4 specific content pillars aligned to expertise |
| X credentials | GitHub secrets | X_API_KEY, X_API_SECRET, X_ACCESS_TOKEN, X_ACCESS_SECRET, X_BEARER_TOKEN |
| Bluesky credentials | GitHub secrets | BLUESKY_HANDLE, BLUESKY_APP_PASSWORD |

## What NOT to do on Template Detection
- Do not create X/Bluesky post files with generic content
- Do not stage queue pairs from placeholder research
- Do not set a fake follower count baseline

## Recommendation for Future Sessions
At session start, check if ME.md contains `[Your Name]`. If so, skip content creation entirely and only do initialization/documentation work.

## Status
- Template detected: 2026-11-08
- Owner action required before next meaningful session
