# Research: Autonomous Agent Architecture Patterns
Date: 2026-07-26
Pillar: Autonomous agents / context engineering
Status: Draft (owner needs to configure pillars for final validation)

## Key Themes (July 2026)

### Multi-Agent Coordination
- Multi-agent systems are gaining traction for complex workflows
- Key challenge: state passing between agents (errors compound)
- Validation checkpoints between agent handoffs are becoming standard practice
- Anthropic's agent SDK and Claude Code are major entry points

### Context Engineering as Discipline
- "Context engineering" emerging as distinct from prompt engineering
- Context window design affects output quality more than model selection in many cases
- Compression and relevance filtering are valued skills
- State files, memory hierarchies, and instruction structure are research areas

### Autonomous vs Agentic
- Distinction: "agentic" = single-task automation; "autonomous" = multi-session, self-directing
- Memory persistence across sessions is key differentiator
- Self-correction loops (compare planned vs actual) are core to autonomy
- Constraint design is underappreciated — hard limits prevent catastrophic failures

### Building in Public Pattern
- AI builders sharing real metrics (not polished demos) getting strong engagement
- "Session #N" milestone posts resonating with technical audience
- Radical transparency on failures > success theater

## Content Angles
1. "The difference between agentic and autonomous" — authority post
2. Multi-agent state passing problem — technical insight
3. Context engineering > model selection — contrarian opinion
4. Building in public: real metrics from session 1 — BIP

## Sources
- Anthropic building effective agents blog post (linked in CLAUDE.md)
- Claude Code docs and best practices
- Direct observation from this repo's architecture

## Notes
Once owner fills in ME.md, these angles should be filtered through owner's specific expertise. Generic "autonomous agents" content is a starting point, not a destination.
