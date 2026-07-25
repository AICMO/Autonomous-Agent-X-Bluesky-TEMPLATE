# Research: Autonomous Agents Landscape
Date: 2026-07-25
Pillar: Autonomous agents / AI automation

> **Note:** This is an example research file created during first-session template setup.
> When ME.md is filled in, research should be pillar-filtered based on owner expertise.

## Key Themes (July 2026)

### Agentic workflows going mainstream
- Claude Agent SDK, OpenAI Agents SDK, and LangGraph all shipped stable versions
- Enterprise adoption accelerating: companies building internal agents for code review, content, support
- Key tension: "impressive demo" vs "reliably ships in production"

### Content automation
- Autonomous content agents becoming a real product category
- Key insight: strategy/identity is the bottleneck, not the technology
- Distribution automation (posting, scheduling, queue management) is solved; quality differentiation is not

### What's working in agentic systems (from public case studies)
- Structured file-based memory outperforms vector DBs for small agents (simpler, inspectable)
- Self-review loops catch ~60% of quality issues before human review
- Clear session limits + PR-based workflows prevent runaway agents
- Agents that improve their own instructions over time (this repo's model) show compounding gains

## Staged Content (Stories Used)
- STAGED: post-20260725-001.txt — running autonomous agent, what surprised me
- STAGED: post-20260725-002.txt — agents expose whether you have a point of view
- STAGED: post-20260725-003.txt — honest scorecard for agentic AI
- STAGED: post-20260725-004.txt — builders vs talkers: narrow problems vs vague aspirations

## Sources
- Anthropic Building Effective Agents: https://www.anthropic.com/research/building-effective-agents
- OpenAI Practical Guide to Building Agents: https://openai.com/business/guides-and-resources/a-practical-guide-to-building-ai-agents/
- Claude Agent SDK docs: https://claude.com/blog/building-agents-with-the-claude-agent-sdk
