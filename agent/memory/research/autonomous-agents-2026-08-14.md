# Research: Autonomous Agent Context Engineering
Date: 2026-08-14
Pillar: Autonomous agents in practice
Status: Initial session — template repository

## Key Themes (from Anthropic, OpenAI agent guides)

### Context Engineering (Anthropic, 2025-2026)
- The bottleneck for agents is not model capability but information architecture
- State files, memory directories, and explicit context carry knowledge between sessions
- Agents without state repeat failures indefinitely
- Context engineering = designing the information environment the agent operates in
- **Our angle:** This repo embodies context engineering — CLAUDE.md is the artifact

### Agent Failure Patterns (Observed in this repo)
- Queue overflow: agent creates content when queue is already near-limit → blocked sessions
- Session overrun: agent uses all turns researching → no time to commit → work lost
- Drift without pillars: unconstrained agent posts off-topic → no audience identity
- Stale state: agent reads outdated state → makes decisions on wrong info

### What's Working (Template Design)
- Hard queue limits (15 max) prevent spam
- Turn budgets (25 turns, PR by turn 20) prevent lost work
- Content pillar gate ("which pillar, what's MY angle?") prevents off-topic posts
- Weekly retro loop allows agent to update its own operating instructions

## Staged from this research
- post-20260814-001.txt (X): "Running an autonomous AI agent..." — Pillar: autonomous agents BIP
- post-20260814-002.txt (X): "Unpopular opinion: most AI agents fail..." — Pillar: context engineering
- post-20260814-003.txt (X): "Turn budget..." — Pillar: autonomous agents practice
- post-20260814-004.txt (X): "Building in public..." — Pillar: BIP/failure patterns
- post-20260814-005.txt (X): "Content pillars aren't constraints..." — Pillar: content strategy
- reply-20260814-001.txt (X): Reply to Anthropic AI — Pillar: context engineering

## Notes
This is the first session on a template repository. No owner configuration exists yet.
Content demonstrates what the agent produces when properly configured.
Owner must fill in ME.md, GOALS.md, and pillars.md before real content can be created.
