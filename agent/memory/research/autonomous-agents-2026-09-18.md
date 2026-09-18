# Autonomous Agent Landscape — 2026-09-18

## Context
Template repository, first session. No owner pillars defined yet. Research focuses on the repo's own domain: autonomous agent design and operation.

## Key Themes (September 2026)

### Agent Loop Design
- OODA (Observe-Orient-Decide-Act) emerging as preferred framework for agent sessions
- Explicit stopping rules increasingly recognized as critical safety primitive
- Turn budget enforcement (25 turns/session) prevents runaway agents
- PR-per-session pattern creates natural checkpoints and audit trails

### Memory Architecture
- File-based persistent state outperforms in-context memory for long-running agents
- State files: operational (current session), hypotheses (beliefs to test), learnings (validated insights)
- Memory bloat is a real problem — agents that don't prune context get slower and dumber
- Target: <500KB total agent memory directory

### Queue Management
- Content queues need hard limits, not soft recommendations
- Look-ahead zone (queue 11-12) as important as hard limit (queue 15)
- Creating 2 files at queue=13 → immediate block in next session (cascading failure pattern)
- Blocked session protocol: tier the work by value, not by default "do nothing"

### Self-Improvement Patterns
- Agents that update their own operating instructions outperform static-instruction agents
- Skill files (permanent, reusable knowledge) vs. learnings (session-specific observations)
- Weekly retrospectives as the primary driver of behavioral improvement
- Evidence standard: don't update skills without data supporting the change

## Pillar Candidates (for this repo's content)
Once ME.md is filled in, likely pillars include:
1. Autonomous agent design and architecture
2. Building in public / transparent AI systems
3. Content automation at scale
4. Agent memory and state management

## Content Angles Not Yet Staged
- STAGED: post-20260918-001 (BIP: running autonomous agent)
- STAGED: post-20260918-002 (opinion: agents vs scripts)
- STAGED: post-20260918-003 (OODA loop design)
- STAGED: post-20260918-004 (queue discipline lesson)
