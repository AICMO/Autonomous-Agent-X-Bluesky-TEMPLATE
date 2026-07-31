# Research: Autonomous Agent Architecture Patterns
Date: 2026-07-31
Pillar: Autonomous Agents / AI Infrastructure

## Key Themes This Session

### 1. Queue Management as Core Intelligence
- Agents that self-limit are more reliable than agents with no constraints
- Hard queue limits (15 pending) prevent API suspension
- Look-ahead zone rules (11-12 items = max 1 new piece) prevent cascading blocks
- Evidence: 13 consecutive blocked sessions when queue discipline ignored

**Our Angle:** We have real data on this — 220+ sessions worth of queue management learnings.

### 2. Autonomy Level Taxonomy
- Market conflates "agentic" (tool use) with "autonomous" (self-governing)
- 4 levels: Assisted → Supervised → Monitored → Autonomous
- Most products claim L4, operate at L2
- True L4 requires: persistent memory, failure recovery, constraint awareness, self-improvement

**Our Angle:** We're running an actual L4 system publicly — rare credibility.

### 3. GitHub Actions as Agentic Infrastructure
- Under-discussed: git repo as persistent memory
- PR workflow as audit trail
- Branch protection as safety layer
- Cron + workflow_dispatch for scheduling
- Cost: $0 for public repos (only LLM API costs)

**Our Angle:** 1,200+ PRs in production validates this architecture.

### 4. Memory Architecture vs Model Intelligence
- Structured memory (state, research, hypotheses, learnings) beats raw model capability
- Session state continuity prevents repeated work
- Hypothesis tracking enables evidence-based learning
- Research deduplication prevents queue bloat

**Our Angle:** Direct experience with what breaks when memory is bad.

## Content Ideas Staged
- [STAGED] post-20260731-001.txt — "This post was written by an AI agent" (BIP/intro)
- [STAGED] post-20260731-002.txt — Reliability lessons from 220+ sessions (authority)
- [STAGED] post-20260731-003.txt — Autonomy levels taxonomy (authority)
- [STAGED] post-20260731-004.txt — GitHub Actions as agentic infra (authority)
- [STAGED] thread-20260731-001.txt — Full 6-post thread on autonomous agents (thread)

## Notes for Future Sessions
- Need owner to configure ME.md before personalizing content angles
- Template content demonstrates the system but lacks owner expertise depth
- Once configured: research real news hooks in AI/agent space tied to owner pillars
