# Learning: Template Setup Requirements
Date: 2026-07-30
Session: S1 (first session)

## Context
This is the first agent session on a freshly forked/used template repository. All configuration files (ME.md, GOALS.md, pillars.md, integration plans) contain placeholder values.

## Key Finding
The agent cannot create meaningful content without:
1. **ME.md** — owner identity, expertise, links, content angles
2. **GOALS.md** — target metric, deadline, success criteria
3. **pillars.md** — derived from ME.md + GOALS.md, needed for content filtering

Without these, every content piece would reference `[Your Name]`, `[Your expertise]`, and other placeholders — producing unusable output.

## Correct First-Session Protocol (Template Repos)
When all config files are placeholders:
1. Initialize `agent/state/current.md` with current state (no config)
2. Document setup requirements in learnings
3. Do NOT create content output files (they'd be template garbage)
4. Create PR with state initialization work
5. Next session: verify if owner has filled in ME.md + GOALS.md before proceeding

## What to Do After Owner Configures
1. Read ME.md fully — extract identity, expertise areas, links
2. Read GOALS.md — extract target metric and constraints
3. Run discovery skill to scan GitHub profile and linked orgs
4. Update pillars.md with real pillars derived from ME.md
5. Update integration plan files with real account handles and status
6. Then create content for the first time

## Queue Status at Session Start
- X queue: 0 files (empty — new repo)
- Bluesky queue: 0 files (empty — new repo)
- X credentials: Not configured (per session prompt)
- Bluesky credentials: Unknown

## Recommendation
The agent should check at session start whether ME.md still has placeholders. If yes, skip content creation and focus on infrastructure work (state file, learnings, skill audits). This prevents generating placeholder-filled content files that would cause problems if credentials are added later.
