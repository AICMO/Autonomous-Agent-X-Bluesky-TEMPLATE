# Learning: Template Setup Requirements
Date: 2026-08-10
Session: S1 (First session)
Status: Active

## Context

This is the first agent session on a fresh template repository. The agent cannot create personalized content because ME.md and GOALS.md contain placeholder text, not real owner information.

## What the Agent Needs to Operate

### Required (Cannot run without)
1. **ME.md** — Completed with real owner info:
   - Name, background, expertise areas
   - Current role and projects
   - All social/professional links (X, Bluesky, GitHub, LinkedIn)
   - Content angles the agent should use

2. **GOALS.md** — Completed with:
   - Specific target metric (followers, stars, etc.)
   - Numeric target and deadline
   - Any constraints

3. **Platform credentials** — At least one of:
   - X: OAuth 1.0a credentials as GitHub secrets
   - Bluesky: App Password as GitHub secrets

### Recommended (Improves quality)
4. **agent/memory/pillars.md** — Can be auto-generated from ME.md on first configured session
5. **agent/integrations/x/plan.md** — Drain rates, queue limits (auto-created first session)

## First-Session Protocol (Post-Configuration)

When ME.md and GOALS.md are configured, the agent's first real session should:
1. Read ME.md fully — extract expertise areas and content angles
2. Generate `agent/memory/pillars.md` from that expertise
3. Web search for 5-10 recent news items in those pillar areas
4. Filter through pillar gate (which pillar? what's my angle?)
5. Write 2-3 content pieces for X + Bluesky versions
6. Start with engagement focus (70% engagement / 30% content at <100 followers)

## Key Insight

The template is well-designed. The agent just needs the owner's identity to function. Don't create generic AI-industry content without knowing which pillars to filter through. Wait for configuration.
