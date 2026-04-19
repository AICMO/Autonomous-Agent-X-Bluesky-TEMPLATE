# Autonomous Agents Research
Date: 2026-04-19
Pillar: Autonomous AI agents / agentic workflows

## Key Themes (April 2026)

### 1. Agent Frameworks Maturing
- Multiple production-ready agent frameworks now available
- Claude Agent SDK, LangGraph, AutoGen, CrewAI all seeing real adoption
- Trend: from "demo agents" to "production agents with constraints"
- Our angle: constraint engineering is the differentiator — anyone can wire up an agent, few can wire one that behaves well long-term

### 2. Context Engineering as Core Skill
- Growing recognition that prompt engineering is secondary to context engineering
- "What does the agent know?" matters more than "how does the agent reason?"
- Anthropic published on effective context engineering
- Our angle: this repo demonstrates context engineering in practice — ME.md, GOALS.md, pillars.md = the context layer

### 3. Self-Improving Agents
- Agents that update their own instructions (within guardrails) are a hot topic
- Distinction between "agent improves output" vs "agent improves itself"
- Safety concern: runaway self-modification
- Our angle: the CLAUDE.md update protocol shows how to allow self-improvement safely — explicit reasoning required, git history preserves all versions

### 4. GitHub as Agent Infrastructure
- Using git repos as agent state stores is an emerging pattern
- Benefits: version history, diffs, PRs = auditable trail
- GitHub Actions as compute substrate
- Our angle: this entire repo is a working demonstration of git-native agent architecture

## Content Opportunities

| Hook | Pillar | Our Angle | Priority |
|------|--------|-----------|----------|
| "Context engineering > prompt engineering" | Agent architecture | ME.md + context files demonstrate this | HIGH |
| "Git as agent memory" | Agentic workflows | Our repo is the proof | HIGH |
| "Self-improving agents safely" | Agent design | CLAUDE.md update protocol | MEDIUM |
| "Constraints matter more than capabilities" | Agent architecture | Queue limits, turn limits, hard bans | HIGH |

## Notes
- All hooks above staged in `agent/outputs/x/` for this session
- Review engagement on these posts to validate which pillar angles resonate
- Next research session: check for new agent framework releases, benchmark comparisons
