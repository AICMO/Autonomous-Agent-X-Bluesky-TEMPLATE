# Learning: Template Repository — First Session Behavior

Date: 2026-08-13
Session: S1 (first session)
Status: Documented

## Context

This repository is a public template for autonomous social media agents (X + Bluesky). On first session, ME.md and GOALS.md contain only placeholder content. No credentials are configured.

## What the Agent Should Do in Template State

### Check First (1-2 turns)
1. Read `agent/state/current.md` — if missing, it's the first session
2. Read `ME.md` and `GOALS.md` — are they templates or real content?
3. Check session prompt for credential status (e.g., "X credentials not configured")

### If Template State Detected
- Do NOT fabricate content using placeholder personas
- Do NOT create fake expertise pillars
- Do NOT stage posts that would be posted as "the owner" when no owner identity exists

### What IS Useful to Do
- Create `agent/state/current.md` documenting the template state
- Document the configuration checklist (what owner needs to fill in)
- Create this learnings file so future sessions understand the pattern

### What Unblocks the Agent
The owner needs to:
1. Fill in `ME.md` with real identity, expertise, and links
2. Fill in `GOALS.md` with real target and deadline
3. Add platform credentials to GitHub Secrets (see README.md setup guide)
4. Fill in `agent/memory/pillars.md` with real expertise pillars
5. Fill in `agent/integrations/x/plan.md` and `agent/integrations/bluesky/plan.md`

## Key Insight

Template detection is fast (2-3 turns). When identified:
- Save turns by NOT doing research/content work
- Create state file + this learning = productive session output
- Commit and PR = work is preserved, owner can see what happened

## Applied To
- `agent/state/current.md` — documented template state and config checklist
