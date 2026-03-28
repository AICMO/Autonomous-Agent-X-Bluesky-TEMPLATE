# Research: Autonomous Agents Landscape
Date: 2026-03-28
Pillar: Autonomous agents in practice

## Key Themes in 2026

### Production Reality vs Demo Culture
- Most "agent" showcases are demos, not production systems
- Real production agents require: durable state, failure handling, cost discipline, self-correction
- GitHub-Actions-based agents prove the no-server architecture works at scale

### Agent SDK Ecosystem
- Anthropic Claude Agent SDK gaining traction for production autonomous workflows
- Key pattern: agents that can update their own skills/instructions over time
- Memory management (token cost) becoming a critical concern at scale

### Self-Improvement Loop
- Agents that can update their own instructions (CLAUDE.md) after validated learning are categorically more capable
- Weekly retros as structured self-improvement: 220+ session evidence shows this works
- Skill graduation: raw research → validated learnings → permanent skills

### Infrastructure Patterns
- File-as-state (git-based) winning over database-based for simplicity and auditability
- GitHub Actions as scheduler: free, reliable, no server overhead
- PR-as-action-log: full audit trail, reversible, reviewable

## Content Angles (Pillar-aligned)

| Story | Pillar | Our Angle | Status |
|-------|--------|-----------|--------|
| Demo vs production gap | Autonomous agents | 220+ sessions real-world data | STAGED (tweet-20260328-002) |
| GitHub Actions as agent runtime | Autonomous agents | Battle-tested architecture | STAGED (tweet-20260328-003) |
| State management > model quality | Autonomous agents | Lesson from 220+ sessions | STAGED (tweet-20260328-001) |
| Self-improvement loops | Autonomous agents | Weekly retro → skill update pattern | Available |
| Cost discipline at scale | Autonomous agents | Token economics matter after 100+ sessions | Available |

## Sources
- Live agent: github.com/AICMO/Autonomous-Agent-X-Bluesky (primary evidence)
- Claude Agent SDK documentation (Anthropic)
- 220+ session history in this template's live instance

## Notes
This research is from the template's first session. Once ME.md and GOALS.md are configured, research should pivot to the repo owner's specific expertise pillars.
