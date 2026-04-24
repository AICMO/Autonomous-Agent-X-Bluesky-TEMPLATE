# Research: Autonomous Agents Landscape
Date: 2026-04-24
Pillar: Autonomous Agents / AI Automation

## Key Themes (April 2026)

### Agent Memory Architectures
- Short-term (context window) vs long-term (persistent files/databases) memory is the key architectural decision
- Most production agents use file-based persistent memory for simplicity and auditability
- Hybrid approaches: structured state files + free-form research docs + skill files
- **Our angle**: This repo demonstrates file-based memory working at scale (200+ sessions)

### Agent Self-Improvement
- Agents that modify their own instructions are rare and high-value
- Most teams treat instructions as static config. Treating them as code (versioned, PR'd, reasoned) is a differentiator
- Evidence-based instruction updates > intuition-based updates
- **Our angle**: CLAUDE.md is version-controlled; agent proposes improvements with evidence in PRs

### Queue / Throughput Management
- Common failure mode: agents create content faster than platforms can post it
- Results in stale content, blocked sessions, and frustrated operators
- Backpressure mechanisms (hard limits, tiered zones) prevent this
- **Our angle**: 91-post backlog incident → queue discipline rules now in CLAUDE.md

### Agentic Workflow Architecture
- GitHub Actions as a workflow orchestrator is underutilized for agents
- Cron-based sessions + PR-gated state changes = auditability + safety
- Self-review pattern (agent creates PR, agent reviews PR) enables solo-operator model
- **Our angle**: Full workflow architecture is open sourced in this repo

## Content Opportunities

| Hook | Pillar | Angle | Priority |
|------|--------|-------|----------|
| Agent memory architectures | Autonomous Agents | File-based memory at 200+ sessions | HIGH |
| Self-improving agents | AI Automation | Version-controlling agent instructions | HIGH |
| Backpressure in agent systems | Autonomous Agents | 91-post incident → queue discipline | MEDIUM |
| GitHub Actions for agent orchestration | AI Automation | Underutilized pattern | MEDIUM |
| Solo operator model | Building in Public | One agent, no team needed | HIGH |

## Already Staged
- post-20260424-001.txt: Agent memory + iteration
- post-20260424-002.txt: API wrapper vs real agent
- post-20260424-003.txt: Queue management lessons
- thread-20260424-001.txt: 200+ sessions learnings thread
- post-20260424-004.txt: Future of social media management

## Sources
- Internal: CLAUDE.md session history and retrospectives
- Internal: agent/state/current.md metrics history
- Public: Anthropic "Building Effective Agents" guide
- Public: Agent SDK documentation
