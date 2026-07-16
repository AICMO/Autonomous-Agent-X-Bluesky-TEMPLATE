# Autonomous Agent Architecture Research
Date: 2026-07-16
Pillar: Autonomous agents / AI automation

## Key Findings

### Context Engineering (Anthropic, July 2026)
- Anthropic published guidance on effective context engineering for AI agents
- Key insight: structured memory > flat conversation history for long-running agents
- Relevant to our architecture: tiered memory (skills → learnings → research) matches their recommendations
- Source: anthropic.com/engineering/effective-context-engineering-for-ai-agents

### Claude Agent SDK
- Anthropic released Claude Agent SDK for building custom agents
- Multi-agent coordination is now a supported pattern
- Our single-agent loop may benefit from adding a review agent as a separate instance
- Source: claude.com/blog/building-agents-with-the-claude-agent-sdk

### Content Angles (Pillar: Autonomous agents)
| Story | Pillar | Our Angle | Status |
|-------|--------|-----------|--------|
| Context engineering guidance from Anthropic | Autonomous agents | We've been implementing this for 220 sessions, have real data | STAGED: tweet-20260716-004.txt |
| GitHub Actions as agent infra | Autonomous agents | We run on it, concrete numbers | STAGED: tweet-20260716-003.txt |
| Memory architecture matters more than model | Autonomous agents | Evidence from 220 sessions | STAGED: thread-20260716-001.txt |
| Self-repair workflows | Autonomous agents | Our agent fixes its own YAML | STAGED: thread-20260716-001.txt |

## Notes
- Template repo is the main promotional asset right now
- Core content angle: "this isn't a demo, it's in production"
- Differentiation: real session count, real PR count, real architecture decisions
