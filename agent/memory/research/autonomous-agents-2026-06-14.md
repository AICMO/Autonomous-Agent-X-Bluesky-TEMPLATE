# Research: Autonomous Agents — State of Play
Date: 2026-06-14
Pillar: Autonomous agents / AI automation

## Key Themes

### 1. Agent Memory Architecture
- Structured state files outperform infinite context for long-running agents
- Key insight: What NOT to remember is as important as what to remember
- Best practice: Maintain metrics, planned steps, retrospectives — discard implementation details

### 2. Compounding Improvement
- Agents that can modify their own instructions improve over time
- Requires: documented reasoning for every change (prevents drift)
- Evidence from this template: CLAUDE.md has been updated based on agent-discovered patterns

### 3. Feedback Loop Design
- PR-per-session creates natural checkpoints and accountability
- Next session reading previous session's PR creates continuity without bloat
- Public PRs = transparency into agent behavior

### 4. Common Failure Modes
- Queue bloat: producing content faster than it gets posted
- Metric theater: optimizing for activity (posts created) vs outcomes (engagement)
- Stale blockers: marking things blocked, never rechecking
- Vague goals: agent optimizes precisely for what's specified

### 5. Cost Structure
- Infrastructure: GitHub Actions free tier covers most workloads
- LLM API: $5-15/month for 9 sessions/day at typical token usage
- Setup cost: ~1 weekend to configure and understand the system

## Content Angles
- "Real agents vs scripts with GPT calls" — clear differentiation content
- "The compounding mechanism" — why session 100 is better than session 1
- "Failure modes nobody talks about" — high engagement, honest format
- "Cost breakdown" — concrete numbers always perform well

## Notes
Template-specific: this research is based on the template's own design principles, not external sources. Once the owner fills in ME.md, research should shift to their specific domain.
