# Learning: Template Initialization
Date: 2026-06-27
Session: S1 (first session)

## Context
This is the first agent session on a fresh template fork. No owner configuration exists yet.

## What the Agent Observed
- ME.md: placeholder template (no owner info)
- GOALS.md: placeholder template (no goal defined)
- agent/state/current.md: did not exist
- agent/outputs/x/: empty (queue = 0)
- agent/outputs/bluesky/: empty (queue = 0)
- agent/memory/pillars.md: placeholder template

## Key Insight: Template-First Sessions Have No Content Work
When ME.md and GOALS.md are unfilled placeholders, the agent cannot:
- Discover content pillars (no owner expertise defined)
- Create on-pillar content (no pillars = no pillar gate to check against)
- Post to platforms (no credentials configured)

The correct behavior in this state: **initialize foundational files and document the setup requirements.**

## Setup Prerequisites (Ordered)
1. **Fork the repo** — done (this session is running)
2. **Fill ME.md** — owner identity, expertise, links, current projects
3. **Fill GOALS.md** — target metric, deadline, success criteria
4. **Add ANTHROPIC_API_KEY secret** — required for agent sessions to run
5. **Add platform credentials** (optional):
   - X: X_API_KEY, X_API_SECRET, X_ACCESS_TOKEN, X_ACCESS_TOKEN_SECRET
   - Bluesky: BLUESKY_HANDLE, BLUESKY_PASSWORD
6. **Configure branch ruleset** — "Require a pull request before merging" (see README.md)
7. **Enable GitHub Actions** — ensure workflows can run

## After Owner Configures
The next session should:
1. Read ME.md → discover expertise pillars
2. Read GOALS.md → understand target metric
3. Create agent/memory/pillars.md with discovered pillars
4. Run web search for pillar-relevant news
5. Create first content pieces

## Lesson for Future Sessions
If ME.md contains placeholder text (`[Your Name]`, `[Your Goal]`), skip content creation entirely and document the configuration gap. Do not fabricate owner information for content.
