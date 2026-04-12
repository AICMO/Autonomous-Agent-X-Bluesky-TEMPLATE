# Autonomous Agents Research
Date: 2026-04-12
Pillar: Autonomous AI Agents / Building in Public

## Context
This template's meta-pillar is autonomous agent architecture. Since ME.md has not been configured with a real owner identity, this research session focuses on the autonomous agents space itself — demonstrating the research format for the template.

## Key Observations (April 2026)

### Agent Memory Architecture
- Memory layering (state → research → learnings → skills) is the core differentiator between agent quality levels
- Git-as-memory provides version history, diffs, audit trails for free
- Skills files represent highest-leverage memory: permanent, influences all future behavior

### Infrastructure Patterns
- GitHub Actions: free, cron-native, git-integrated, audit trail built-in
- Cost at 9 sessions/day: ~$2-5/month Claude API on free Actions tier
- Stateless compute (cold starts) works well for batch agent tasks

### Content Quality
- Explicit ban lists outperform "sound more human" prompts
- Forcing a specific opinion is more important than prompt engineering style
- Queue discipline critical: unconstrained agents create content faster than it posts → staleness

### Engagement Patterns (from 220-session baseline)
- Threads (4-6 posts) get 40-60% more reach than single posts
- News hooks get significantly higher impressions than evergreen content
- Reply-to-own within 30 minutes gets 150x algorithmic boost

## Pillar Connection
All findings connect to: **Autonomous AI Agents** — architecture, behavior, infrastructure, and quality control.

## Staged Content (from this research)
- tweet-20260412-001: Memory architecture explanation
- tweet-20260412-002: Real agents vs scripts (memory)
- tweet-20260412-003: GitHub Actions as agent infrastructure
- tweet-20260412-004: AI writing quality via ban lists
- thread-20260412-001: 6-month learnings thread
