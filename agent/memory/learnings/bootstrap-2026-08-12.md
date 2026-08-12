# Learning: Template Bootstrap State

Date: 2026-08-12
Session: S1 (first session)
Status: Reference

## Situation

First agent session on a fresh template repository. Found the following unconfigured:

- **ME.md** — All fields are placeholders (name, background, expertise, links)
- **GOALS.md** — Template structure with no actual targets
- **agent/state/current.md** — Did not exist (created this session)
- **agent/memory/pillars.md** — Template pillars with no real content
- **Platform integrations** — X credentials not configured, Bluesky not configured
- **Output queues** — Empty (X: 0, Bluesky: 0)

## Key Insight

An unconfigured template means the agent cannot:
1. Create meaningful content (no owner voice/context)
2. Post content (no API credentials)
3. Track progress toward goals (no goals defined)

The correct response is NOT to generate generic placeholder content. Generic content would be:
- Off-brand (no owner identity to represent)
- Unpostable (no credentials)
- Wasted work

## What to Do When Blocked by Template State

1. Initialize the state file (done this session)
2. Document the blockers clearly
3. Create a minimal PR to signal the agent ran and detected the state
4. Do NOT create fake content to hit session targets

## Required Owner Actions Before Agent Can Operate

1. Fill in `ME.md` — name, background, expertise, links, GitHub profile
2. Fill in `GOALS.md` — specific metric targets, deadlines
3. Add GitHub Secrets for X API (see README for required secrets)
4. Add GitHub Secrets for Bluesky API (see README for required secrets)
5. Optionally join X Communities aligned with content pillars

## Next Session Behavior

If ME.md and GOALS.md are still templates in the next session:
- Check if credentials are now configured (`gh variable list`)
- If still unconfigured, skip content creation
- Do NOT create PRs with only state file timestamp updates
- If nothing meaningful to commit, do not create a PR

## Graduation Criteria

This file can be deleted once:
- ME.md is fully configured
- GOALS.md has real targets
- First real content session has been completed
- Learnings from actual operation supersede this bootstrap doc
