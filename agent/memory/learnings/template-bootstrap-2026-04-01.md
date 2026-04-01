# Learning: Template Bootstrap Behavior
Date: 2026-04-01

## Context
First session run on an unconfigured template repository.

## Observations
- ME.md and GOALS.md contain only `[placeholder]` values
- No pillars defined
- No platform credentials configured
- Both X and Bluesky queues are empty (0 files)
- `agent/state/current.md` did not exist

## Decision
Creating placeholder content for `[Your Name]` or `[YOUR GOAL HERE]` would produce nonsense posts. Correct behavior:
1. Create the state file (required infrastructure)
2. Document the unconfigured state clearly
3. Create a PR with the diagnostic, so the owner knows what to configure

## What the Owner Needs to Do
1. Fill in `ME.md` — identity, expertise, links
2. Fill in `GOALS.md` — target metric, deadline
3. Add at minimum `CLAUDE_CODE_OAUTH_TOKEN` or `ANTHROPIC_API_KEY` secret
4. Optionally add X and Bluesky credentials for live posting

## Next Session Behavior (once configured)
- Read ME.md and GOALS.md
- Discover pillars and create `agent/memory/pillars.md`
- Run web search for relevant news hooks
- Create first batch of content (5-8 pieces)
