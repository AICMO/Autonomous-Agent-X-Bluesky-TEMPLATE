# Autonomous Agents Research
Date: 2026-03-26
Pillar: Autonomous agent building
Session: Initial (S1)

## Key Themes in AI Agent Development (March 2026)

### Memory Architecture
- External persistent memory (files, databases) vs. in-context memory is the critical design decision
- Agents that rely solely on context window fail to compound learning across sessions
- File-based memory (GitHub repo) works well for agents with moderate state requirements
- Pattern: Learnings → Skills (distilled playbooks) → Context (ephemeral session state)

### Self-Improvement Loops
- Retrospective-driven improvement: agents that write weekly retros and update operating instructions get measurably better
- Signal is noisy: need 50+ sessions before reliable patterns emerge
- Compounding improvement at machine speed is the value proposition

### Infrastructure Patterns
- GitHub Actions as orchestration layer eliminates server costs ($0-5/month infra)
- State-as-files pattern: no database needed for moderate state requirements
- Queue management critical: content pipelines need hard limits to prevent bloat

### Common Failure Modes
1. No retrospective loop → agent repeats known mistakes
2. Context window stuffing instead of proper memory → quality cliff at ~100K tokens
3. "Agency theater" — LLM pipelines labeled as agents without real feedback loops
4. Queue discipline failures → content backlog overwhelming drain capacity

## Content Angles Used
- Architecture explanation (tweet-001): How autonomous agent works at a high level
- Opinion/take (tweet-002): Real vs fake agents — retrospective as the test
- Tactical/how-to (tweet-003): GitHub Actions infra cost breakdown
- Mental model (tweet-004): Context window ≠ memory
- Thread/lessons (tweet-005): 220-session learnings summary

## Notes
- All content based on this repo's demonstrated architecture (220+ sessions documented in README)
- Template ME.md not yet configured — content uses generic "autonomous agent building" pillar
- Owner should configure ME.md + GOALS.md to enable domain-specific content
